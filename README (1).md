# ExamEase – Smart Exam Scheduler (Modified)

## New features
- Student Year, Department and Section
- Dynamic room allocation
- Avoids reusing a student's previous room when possible
- Intelligent seat allocation
- Same-exam adjacent-seat conflict checking
- Year/department-aware seating preferences
- Visual seating arrangement
- Student venue lookup
- Student hall-ticket style venue card
- QR venue records
- QR download/print
- Timetable + seating + QR CSV export
- Existing localStorage workflow preserved

## Run
1. Open this folder in VS Code.
2. Open `index.html`.
3. Use Live Server if available.
4. Click **Generate / Repair Schedule**.
5. Click **Generate Seating**.
6. Open **Student Venue** to test a student lookup.
7. Open **QR Management** to view/print QR records.

## QR update
- QR codes are now **real, scannable QR codes** (built-in offline encoder, no internet needed).
- In **QR Management**, click **View QR** on a student and scan it with a phone camera.
- Default QR content is the student's seating details (name, exam, date, time, building/room, seat), so it works on any phone without a server.
- Optional "Venue link" mode encodes a URL instead; this only works for other devices once the site is hosted online.
- Fixed a bug where a duplicate old `<script>` block caused a `'$' has already been declared` error, which stopped the new features (seating, venue, QR) from running at all.

## Important prototype note
The QR image is generated locally so the demo works without an external QR service. For production deployment, use a standards-compliant QR library/backend and store secure server-side tokens rather than relying on browser localStorage.
