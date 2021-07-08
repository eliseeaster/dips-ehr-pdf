<script>
    import {oauth2 as Smart} from 'fhirclient';
	import {onMount} from 'svelte';

    onMount(async () => {
		Smart.authorize({
			clientId: 'dips-ehr-images',
			scope: 'launch launch/patient patient/DocumentReference.write patient/DocumentReference.read patient/Patient.read patient/encounter patient/resource online_access openid fhirUser',			
			redirectUri: './app',			

			iss:		  'https://dev-tst.dips.fhir.service.api.dips.no',
			launch:		  '6c5d9ca9-54d7-42f5-bfae-a7c19cd217f2::DocumentReference/c1c5fdad-eda4-4e9d-89b0-2a7d8eed45cb',
			<!--launch:		  '6c5d9ca9-54d7-42f5-bfae-a7c19cd217f2::'
			launch:		  'patientId:encounterId:fhirResource'-->
			

			<!--https://dev-tst.dips-ehr-pdf.api.dips.no/?iss=&launch=6c5d9ca9-54d7-42f5-bfae-a7c19cd217f2::DocumentReference/c1c5fdad-eda4-4e9d-89b0-2a7d8eed45cb*/-->

		});
	});
</script>        