.. _notes:

Quick Notes
======================




* The whole project will be under "apps".
* Each app will be standalone containing both the backend "Django" and frontend "React". Needless to say, some apps might include one and not the other.
* App Structure:
  - ```analytics``` includes the general analytics feature that might be interested for stakeholders, insurance companies, or pharmaceuticals. We shall run basic analytics in it.
  - ```assets``` includes some helper functions. Models for speciality, city, disease, gender ...etc.
  - ```auth_``` includes our custom authentication and permissions that will be used on project-wide basis.
  - ```dentist``` includes clinic management platform that is tailored to dentists. Models like Clinic, AdminClinic, Assistant shall be included as well. Similarly, other physicians will have their own.
  - ```drug```
  - ```home```
  - ```insurance```
  - ```internal``` This is for our internal tools.
  - ```patient``` including patient records, prescriptions, treatment plans ...etc.
  - ```qrcode_``` mainly to be used for generating prescriptions.
  - ```supplier```
  - ```visit``` managing patients' visits.
* Most of the APIs require tokens, head to ```api/token``` to generate one.