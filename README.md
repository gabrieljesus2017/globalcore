<h1 align="left"> 📦 PRODUCTO : AP COLECTIVO </h1> <br><br>



<h1 align="center"> 🚀 CONSIDERACIONES PREVIAS </h1> <br>
<p> Por favor tener en cuenta las siguientes validaciones y/o configuraciones, antes de iniciar la migración de componentes </p> <br>



<!-- 1 ------------------------------------------------------------------------------------------------------------------------------ -->

## 1. Deliverability

Configure los ajustes en esta página para mejorar la capacidad de entrega de correo electrónico:

* Setup
* Email
* Deliverability
* Access level : Seleccionar la opción "all email" y guarde el cambio
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Deliverability.png?raw=true" width=400>
	</p>
<br>
<br>

<!-- 2 ------------------------------------------------------------------------------------------------------------------------------ -->

## 2. OmniStudio : Metadata & Runtime

Inactivar opciones Metadata & Runtime:

* Setup
* Feature Settings
* Omni Interaction
* OmniStudio Settings
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/OmniStudio%20Settings.png?raw=true" width=500>
	</p>
<br>
<br>

<!-- 3 ------------------------------------------------------------------------------------------------------------------------------ -->

## 3. OmniStudio : Warning URL para LWC

Crear URL correspondientes a las Flex Card:

* App Launcher
* OmniStudio
* OmniStudio FlexCards
* Warnings
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/FlexCardsWarnind.png?raw=true" width=500>
	</p>


* Abra el mensaje: Para obtener las URLS a crear. (Copiar las 2 direcciones).
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/FlexCardSurls.png?raw=true" width=500>
	</p>

Acceda a Remote Site Settings:

* Setup
* Security
* Remote Site Settings
* New Remote Site
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/FlexCardSurlsNew.png?raw=true" width=500>
	</p>

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Remote%20Site%20Settings.png?raw=true" width=500>
	</p>

	Nota: La URL debe hacer referencia a los datos del ambiente de producción.
	
	| Remote Site Name  | Remote Site URL  |
	| ------------ | ------------ |
	| FlexCardLightningForce  |  https://globalseguros--qa.sandbox.lightning.force.com |
	| FlexCardVisualForce  | https://globalseguros--qa--vlocity-ins.cs41.visual.force.com  |
<br>
<br>

<!-- 4 ------------------------------------------------------------------------------------------------------------------------------ -->

## 4. Asignar Action Plan a oportunidades

4.1 Migrar el permission set diseñado para otorgar acceso.

* Migrar de TA el permission set Campaign Influence:
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Campaign%20Influence.png?raw=true" width=500>
	</p>


4.2 Asignar el permission set al ADMIN:

* Setup
* Users
* Usuario ADMIN
* Permission Set Assignments
* Edit Assignments
* Asignamos el permission set y se guarde el cambio
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Asignar%20Campaign%20Influence.png?raw=true" width=500>
	</p>

4.3 Activar Opportunity Team Settings [Link](https://help.salesforce.com/s/articleView?id=sf.fsc_action_plans_opportunity_teams.htm&type=5):

* Setup
* En el buscador ingrese: Opportunity Team Settings
* Seleccione: Opportunity Team Settings
* Seleccione: Enable Team Selling y se guarda el cambio
* Elija un page layout (Opportunity (Wallet Share) Layout) y se guarde el cambio
<br>
<br>

<!-- 5 ------------------------------------------------------------------------------------------------------------------------------ -->

## 5. Insurance Settings

Para el correcto funcionamiento del componente Insurance Policy verifique que todos los botones esten activos.

* Setup
* Feature settings
* Financial Services
* Insurance Settings : Verificar que todos los botones esten habilitados.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Insurance%20Settings.png?raw=true" width=500>
	</p>
<br>
<br>

<!-- 6 ------------------------------------------------------------------------------------------------------------------------------ -->

## 6. Checklist Items With Attachments

Esta configuración otorga permisos al momento de adjuntar archivos en el objeto Document Checklist.

* Setup
* Feature Settings
* Document Checklist
* Document Checklist Settings : Activar el boton de Attachments.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Checklist%20Items%20With%20Attachments.png?raw=true" width=500>
	</p>
<br>
<br>

<!-- 7 ------------------------------------------------------------------------------------------------------------------------------ -->

## 7. Checklist Items Botón de Aprobación

Para activar el botón para Aprobación de documentos (entre otros), en el objeto Document Checklist Items: 

* Object Manager
* Objeto : Document Checklist Items
* Page Layouts
* Buttons : Activar el boton de Aprobación.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/Checklist%20Items%20Boto%CC%81n%20de%20Aprobacio%CC%81n.png?raw=true" width=500>
	</p>
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/BotonAprobarDocumentCheckList.png?raw=true" width=500>
	</p>
<br>
<br>

<!-- 8 ------------------------------------------------------------------------------------------------------------------------------ -->

## 8. Migración de Expression Sets

Ya que la unica manera de realizar la migración de los Expression es por medio del Package Manager. Se deben tener en cuenta las siguientes recomendaciones:

8.1 En la ORG de destino no deben existir los Expresion, ni las Decision Matrices a migrar, para validar:

* App Launcher
* Lookup Tables
* Al ingresar: Este objeto debe estar vacío o por lo menos no deben existir las Decision Matrices que se van a migrar.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/LookupTables.png?raw=true" width=500>
	</p>
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/LookupTablesVacio.png?raw=true" width=500>
	</p>

* App Launcher
* Expression Sets
* Al ingresar: Este objeto debe estar vacío o por lo menos no deben existir los Expression Sets que se van a migrar.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSet.png?raw=true" width=500>
	</p>
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetVacio.png?raw=true" width=500>
	</p>	
	
8.2 En la ORG de Desarrollo (TA) se encuentra contruido el Package Manager que permite la migración en otro ambiente. 🚨 Tenga en cuenta la versión del Expression en la cual fue creado el Data Pack, ya que si ha cambiado deben crear uno nuevo invocando la versión nueva.

* Setup
* Apps
* Packaging
* Package Manager: Se encuentran los paquetes creados y con los cuales se realizo la migración a producción.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackage.png?raw=true" width=500>
	</p>	

* Ingresando al Package de interes
* De click en el botón Upload 
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackageSelectPack.png?raw=true" width=500>
	</p>	
 
* Version Name
* Breve descripción: No es necesario ingresar o seleccionar información adicional.
* De click en el botón Upload
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackageUpload.png?raw=true" width=500>
	</p>	

* Automaticamente se genera el link que va a permitir el despliegue en la ORG de destino.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackageURL.png?raw=true" width=500>
	</p>	

* Al abrir el link en otra pestaña, va a solicitar los datos de Login en la ORG de destino.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackageLogin.png?raw=true" width=500>
	</p>	

* Una vez logeado aparece el estado en que se encuentra el paquete, generalmente el mensaje que aparece es porque no se a completado la compilación y se debe esperar unos minutos (5), en este caso el mensaje que aparece es porque en la ORG de prueba ya se encuentra instalado.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackageCantUpgrade.png?raw=true" width=500>
	</p>

* Una vez se realiza la instalación, debe aparecer este mensaje:
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetPackageConfirmacion.png?raw=true" width=500>
	</p>

Se debe acceder a cada Decision Matrices y cargar el archivo de excel con los productos.

* Seleccionamos la Decision Matris
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/LookupTablesSelect.png?raw=true" width=500>
	</p>
  
* Ingresamos a la versión que se encuentra activa
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/LookupTablesSelectVersion.png?raw=true" width=500>
	</p>

* Cargamos el archivo .CSV exportado previamente del ambiente de Origen.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/LookupTablesLoadFile.png?raw=true" width=500>
	</p>

8.3 Si por alguna razón cambia la versión del Expression Set o se crea uno nuevo, es necesario crear un Data Pack, es importante tener en cuenta que antes de iniciar el proceso de creación, 🚨 debe inactivar el Expression Set. 

* Inactivar Expression Set
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetInactar.png?raw=true" width=500>
	</p>

* Setup
* Apps
* Packaging
* Package Manager: Dar clic en el Botón New.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetNew.png?raw=true" width=500>
	</p>

Diligencie los campos solicitados:

* Package Name : Asigne un nombre que permita identificar facilmente el Data Pack
* Language : English
* Description : Se recomienda colocar la versión del expression. 
* Clic en el botón Save
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetDatos.png?raw=true" width=500>
	</p>

* Clic en el botón (Add / Remove / Templates)

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetAddComponente.png?raw=true" width=500>
	</p>  

* En Component type: Busque el de tipo ExpressionSet Definition Version
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetSearchComponente.png?raw=true" width=500>
	</p>  

* Seleccione la versión del Expression que desea migrar
* Clic en el botón (Add to Package)
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetSelectVersion.png?raw=true" width=500>
	</p>  

* verificar que esten todos los componentes
* Clic en el botón Upload
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetVerificaComponentes.png?raw=true" width=500>
	</p>  

Diligencie los campos solicitados:

* Version Name : Asigne un nombre que permita identificar facilmente el Data Pack
* Description : Se recomienda colocar la versión del expression.
* Clic en el botón Upload
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetUpluadVersion.png?raw=true" width=500>
	</p>  

* Una vez creado el Data Pack va a aparecer el link de instalación
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ExpressionSetGeneraLink.png?raw=true" width=500>
	</p>  
<br>
<br>



<!-- -------------------------------------------------------MIGRACIÓN DE COMPONENTES----------------------------------------------------------------------- -->

<h1 align="center"> 🚀 MIGRACIÓN DE COMPONENTES | ORDEN E INVENTARIO  </h1> <br>

<!-- 9 -----------------------------------------------------MIGRACIÓN DE COMPONENTES----------------------------------------------------------------------- -->

## 9. Orden Migración Componentes x Etapa

Se recomienda dividir el plan de implementación en cuatro etapas principales, cada una de las cuales mueve un subconjunto diferente de los metadatos.

| TIPO NIVEL       | COMPONENTE PRINCIPAL          | DEPENDENCIAS                | OBSERVACIONES          |
| ---------------- | ----------------------------- | ----------------------------|------------------------|
| Nivel de Datos   |                               |                             |                        |
|                  | GlobalValueSet                |                             | Se migra por Gearset   |
|                  | CustomObject                  |                             | Se migra por Gearset   |
|                  |                               | FlexiPage / Ligthing Page   | Se migra por Gearset   |
|                  |                               | CustomField                 | Se migra por Gearset   |
|                  |                               | RecordType                  | Se migra por Gearset   |
|                  |                               | ValidationRule              | Se migra por Gearset   |
|                  |                               | ListView                    | Se migra por Gearset   | 
|                  |                               | FieldSet                    | Se migra por Gearset   |
|                  |                               | CompactLayout               | Se migra por Gearset   |
|                  | Static Resources              |                  		 | Se migra por Gearset   |
|                  | Content Assets                |                  		 | Se migra por Gearset   |
|                  | Picklist                      |                  		 | Se migra por Gearset   |
| Programación     |                               |                             |			  |
|                  | ApexClass                     |                             | Se migra por Gearset   |
|                  | Approval Process              |                             | Se migra por ChangeSet |
|                  |                               | Email Template              | Se migra por ChangeSet |
|                  |                               | Workflow Field Update       | Se migra por ChangeSet |
|                  |                               | Workflow Task               | Se migra por ChangeSet |
|                  |                               | Classic Letterhead          | Se migra por ChangeSet |
|                  |                               | Workflow Alert              | Se migra por ChangeSet |
|                  | Flow                          |                             | Se migra por Gearset y se debe verificar que se active |
|                  | Expresion Set                 |                             | Se migra por Datapack  |
|                  |                               | DecisionMatrixVersion       | Se migra por Datapack y se cargar el CSV de manualmente|
|                  |                               | ExpressionSetVersion        | Se migra por Datapack  |
|                  |                               | CalculationMatrix	         | Se migra por Datapack  |
|                  |                               | DecisionMatrix		 | Se migra por Datapack  |
|                  | FlexCard			   |                             | Se migra por Gearset y se debe inactivar y activar |
|                  | OmniScript			   |                             | Se migra por Gearset y se debe inactivar y activar |
|                  |                               | DataRaptor			 | Se migra por Gearset   |
|                  |                               | IntegrationProcedure        | Se migra por Gearset   |
|                  | Product2			   |                             | Se migra por Gearset   |
|                  | DocumentTemplate		   |                             | Se crean manualmente   |
| Presentación     |                               |                             |                	  |
|                  | Lightning web component	   |                             | Se migra por Datapack  |
|                  | Layout		           |                             | Se migra por Datapack  |
|                  | CustomTab			   |                             | Se migra por Datapack  |
| Permisos 	   |                               |                             | 			  |
|                  | Profile                       |     			 | Se migra por Gearset   |
|                  | Roles                         |                             | Se migra por Gearset   |
|                  | Permission Set                |                             | Se migra por Gearset   |
|                  | Permission Set Group          |                             | Se migra por Gearset   |
<br>
<br>

<!-- 10 -----------------------------------------------------LISTA DE COMPONENTES-------------------------------------------------------------------------- -->

## 10. Inventario de Componentes

| TIPO COMPONENTE       | NOMBRE COMPONENTE          	      | API NAME COMPONETE        | DESCRIPCIÓN       	     |
| --------------------- | ---------------------| ---------------------|---------------------|
| Global Value          | Gloval value set ALL       	      |                           | | 
| Objetos               | Account                    	      | Account                   | | 
|                | Opportunities              	      | Opportunity               | | 
|                | Quote                      	      | Quote                     | | 
|                | Contract                  	      | Contract                  | | 
|                | Group Census               	      | GroupCensus               | | 
|                | Group Census Member        	      | GroupCensusMember         | | 
|                | Group Census Member Plan   	      | GroupCensusMemberPlan     | | 
|                | Action Plans              	      | ActionPlan| | 
|                | Actividades Económica Riesgo 	      | ActividadEconomica__c | | 
|                | Contacts                   	      | Contact | | 
|                | Document Check List 		      | DocumentChecklistItem| | 
|                | Producer Commissions                |	ProducerCommission| | 
|                | Producers			      |	Producer                  | | 
|                | Quote Line Item		      |	QuoteLineItem       | | 
|                | Quote Line Item Group Class	      |	QuoteLineItemGroupClass| | 
|                | Quote Line Item Pricing Adjustments |	vlocity_ins__QuoteLineItemPricingAdjustment__c | | 
|                | Contract Group Plan		      |	ContractGroupPlan| | 
|                | Contract Document		      |	vlocity_ins__ContractVersion__c| | 
|                | Insurance Contracts		      |	InsuranceContract| | 
|                | Insurance Policy		      |	InsurancePolicy| | 
|                | Insurance Policy Coverage	      |	InsurancePolicyCoverage| | 
|                | Insurance Policy Participant	      |	InsurancePolicyParticipant| | 
|                | Insurance Policy Assets	      |	InsurancePolicyAsset| | 
|                | GeneralParameters		      |	GeneralParameters__c| | 
|                | Campaign Influence		      |	CampaignInfluence| | 
|                | Ubicacion			      |	Ubicacion__c| | 
|                | PriceBooks		              | PriceBook2| | 
|Product2|Accidentes Personales Cerrado A|Accidentes Personales Cerrado A (45_1_CA / 217e3a7a-e9bb-8c01-dd46-aa088a69626d)| | 
||Accidentes Personales Cerrado B|Accidentes Personales Cerrado B (45_1_CB / 48aac1a2-88fb-5963-277e-d9664df5775d)| | 
||Accidentes Personales Cerrado C|Accidentes Personales Cerrado C (45_1_CC / 6c7be480-53b0-4c41-eb29-71715ef23b11)| | 
||Accidentes Personales Cerrado D|Accidentes Personales Cerrado D (45_1_CD / 6377c711-c1aa-565c-0972-f1f274c078db)| | 
||Accidentes Personales Colectivos Abierto A|Accidentes Personales Colectivos Abierto A (APC_root / 34be020d-ec08-acbd-e849-1102ab0611ef)| | 
||Accidentes Personales Colectivos Abierto B|Accidentes Personales Colectivos Abierto B (APC_root / eaa9effd-6a09-635f-f816-fa7a5951d778)| | 
||Accidentes Personales Colectivos Abierto C|Accidentes Personales Colectivos Abierto C (APC_root / 61e68223-05a3-9d04-83af-5a5d3f6b1ec4)| | 
||Accidentes Personales Colectivos Abierto Censo|                    | | 
||Gastos médicos por accidente|Gastos médicos por accidente (Cov_GastosMedicosAccidente / 065a28df-633c-4a21-2b4a-25a4246b14f0)| | 
||Gastos médicos por accidente|Gastos médicos por accidente (Cov_GastosMedicosAccidente_Ab / 414b6cb7-b05d-347f-9ed4-197a4bf126e6)| | 
||Renta diaria por Incapacidad Temporal por accidente|Renta diaria por Incapacidad Temporal por accidente (Cov_RentaDiariaIncapacidadTemporal / e4700187-bef3-af68-c9af-36e315762f78)| | 
||Renta diaria por Incapacidad Temporal por accidente|Renta diaria por Incapacidad Temporal por accidente (Cov_RentaDiariaIncapacidadTemporal_Ab / e86d3b8a-3365-d695-0643-40a22d25547d)| | 
||Pérdidas orgánicas por accidente|Pérdidas orgánicas por accidente (Cov_PerdidasOrganicasAccidente_Ab / 0285839c-3ee4-d73d-0c86-4407714f67f1)| | 
||Pérdidas orgánicas por accidente|Pérdidas orgánicas por accidente (Cov_PerdidasOrganicasAccidente / e2da2cb2-dbf4-bcad-a4b1-e84ea73c8bc9)| | 
||Incapacidad Total y Permanente Accidental|Incapacidad Total y Permanente Accidental (Cov_IncapacidadTotalPermanenteAccidental / 75f7b389-db81-0ca2-6718-22c288ba3a20)| | 
||Muerte Accidental|Muerte Accidental (Cov_MuerteAccidental / 69daae6d-33e5-f91b-0eb4-a7e44755ff8a)| | 
||Muerte Accidental|Muerte Accidental (Cov_MuerteAccidental_Ab / 87d74cd7-0a3a-40e5-0753-68fa8da29cff)| | 
||Muerte Accidental con Homicidio|Muerte Accidental con Homicidio (Cov_MuerteAccidentalHomicidio_Ab / e12adf5c-dc32-548f-4c88-c98e004ec88c)| | 
||Muerte Accidental con Homicidio|Muerte Accidental con Homicidio (Cov_MuerteAccidentalHomicidio / 1b01d954-1f1d-f7a5-f91f-475f525afe65)| | 
||Renta diaria por hospitalización por accidente|Renta diaria por hospitalización por accidente (Cov_RentaDiariaHospitalizacionAccidente / 25b1f164-7aa6-3522-a41c-9c80695d310a)|| 
||Renta diaria por hospitalización por accidente|Renta diaria por hospitalización por accidente (Cov_RentaDiariaHospitalizacionAccidente_Ab / f18d7cee-ad58-5a17-da65-e0e099cf7e28)| | 
||Renta diaria por Incapacidad Temporal por accidente|Renta diaria por Incapacidad Temporal por accidente (Cov_RentaDiariaIncapacidadTemporal / e4700187-bef3-af68-c9af-36e315762f78)| | 
||Renta diaria por Incapacidad Temporal por accidente|Renta diaria por Incapacidad Temporal por accidente (Cov_RentaDiariaIncapacidadTemporal_Ab / e86d3b8a-3365-d695-0643-40a22d25547d)| | 
|Expression Set|CPopen_AP|https://globalseguros--ta.sandbox.lightning.force.com/lightning/setup/Package/033D4000000DoJd/view| | 
||CP_AP_Plan|https://globalseguros--ta.sandbox.lightning.force.com/lightning/setup/Package/033D4000000DoJ9/view| | 
|FlexCard|Flex_EnrollmentCMListReview_OS|                    | | 
||Flex_BulkEnrollmentSummary_OS|                    | | 
||Flex_BulkEnrollmentSummaryChild|                    | | 
||Flex_BulkEnrollmentSummaryFailedList|                    ||  
||Flex_OpportunityActions|                    | | 
||Flex_PolicyActions|                    | | 
||Flex_QuotesActions|                    | | 
||Flex_SarlaftDocument|                    | | 
||Flex_ContractActions|                    | | 
||Flex_CreateCensus|                    | | 
||Flex_QuoteActions|                    | | 
||Flex_QuoteActionsContract|                    ||  
||Flex_QuoteDocActions|                    | | 
||Flex_QuoteGroupLife|                    | | 
||Flex_RequestDocument|                    | | 
|Omniscripts|Planes Cotizacion|ClbInsOs_Quote_English|Flujo cotización Vida Grupo| 
||CreateContract|ClbInsOs_CreateContract_English|Flujo creación de contrato|  
||ContractProposal|ClbInsOs_ContractProposal_English|Flujo emisión documentó del contrato|  
||Census|ClbInsOs_CensusQuote_English|Flujo enrolamiento del censo| 
||PolicyCertificate|ClbInsOs_PolicyCertificate_English|Flujo emisión documentó de la póliza|  
||Single Doc - DOCX (LWC)|docGenerationSample_singleDocxLwc_English|Generación documentó cotización|  
||singleDocxLwcContract|docGenerationSample_singleDocxLwcContract_English|Generación documentó contrató| 
||singleDocxLwcPolicy|docGenerationSample_singleDocxLwcPolicy_English|Generación documentó póliza| 
||clbInsOsRequestDocum|ClbInsOs_RequestDocument_English|Flujo creación de documentos|
||Planes Cotizacion VG |ClbInsOs_QuoteGroupLife_English|Flujo cotización Vida Grupo| 
||CreateQuoteDocument|ClbInsOs_CreateQuoteDocument_English|Generación de documento cotización| 
|DataRaptor|SearchByOpportunityId|                    | |
||SaveProducer|                    | |
||TestInputData|                    | |
||OpportunitySave|                    | |
||ExtractDataQuote|                    | |
||clb_ins_ap_QuotingInputs|                    | |
||clb_ins_UpdateQuote|                    | |
||ExtractQuoteLineItems|                    | |
||TransformQuoteLineItems|                    | |
||clb_ins_os_filterProducts_createContract|                    | |
||clb_ins_os_ExtractgetAccountDetailsforContract|                    | |
||TransProductDetailsContract|                    | |
||clb_ins_os_ TransForContract_CreateContract|                    | |
||clb_ins_os_ContractUniqueName_createContract|                    | |
||clb_ins_os_changeQuoteStatus|                    | |
||GetAccountDetails|                    | |
||createCensus|                    | |
||clb_ins_os_ReadCensusMemberError|                    | |
||clb_ins_os_readCensusMemberPlans|                    | |
||clb_ins_os_transCensusMemberPlans|                    | |
||clb_ins_os_ContractEnrollmentCensus_OS|                    | |
||clbInsOsExtractDataPolicy|                    | |
||clbInsOsTransformDataPolicy|                    | |
||clbInsOsExtractContractDetailsNew|                    | |
||clbInsTransformContractJson|                    | |
||clbInsOsExtractPolicyDetails|                    | |
||clbInsTransformPolicyJson|                    | |
||clbInsTransformtDetailsFromQuoteToSlip|                    | |
||clbInsExtractsPolicyIndividual|                    | |
|IntegrationProcedure|clb_ins_ap_internal_process_UpdateQuoting|                    | |
||ClbInsOs_contractMergeAttributes|                    | |
||ClbInsOs_CreateContractAndCensus|                    | |
||checkCensusError|                    | |
||clbInsOsTransformDataPolicy|                    | |
||clb_ins_ap_internal_process_UpdateQuoting|                    | |
||clb_ins_integration_BRIDGERAPIGEE|                    | |
||clb_ins_integration_SVIAPIGEE|                    | |
||clb_ins_integration_bg_getselectedpolicyDetails|                    | |
||ClbInsOs_checkGroupCensusError|                    | |
||ClbInsOs_contractMergeAttributes|                    | |
||ClbInsOs_CreateGroupContractAndCensus|                    | |
||ClbInsOs_UpdateQuoteContract|                    | |
||clbinsContract_Template|                    | |
||clbInsPolicy_Template|                    | |
|Flow|clbInsOsUpdateContractGroupPlan|                    | |
||clbInsOsUpdateContractGroupPlanOpen|                    | |
||clbInsOsCreatePolicyHolderAndAsset|                    | |
||clbInsOsReceiveValueInsured|                    | |
||clbInsOsCloseActionPlan|                    | |
||clbInsOsChangeQuoteSatusClosed|                    | |
||clbInsOsChangeStatusDocumentQuote|                    | |
||clbInsOsAlertChangeField|                    | |
||clbInsOs_updateCensusMemberName|                    | |
||Approval_Trigger_for_Quote_Open_Plans|                    | |
||AprrovalClosedPlanQuote|                    | |
||Approval_Process_for_Commissions|                    | |
||clbInsOsDocumentRejectedNotification|                    | |
||clbInsOsDocumentApprovedNotification|                    | |
||clbInsOsQuoteRejectedNotification|                    | |
||clbInsOsQuoteApprovedNotification|                    | |
||createProducerforContact|                    | |
||clbInsOsUpdateGroupCensusMember|                    | |
|Approval Process|Quote.Aprobacion_Plan_Abierto||Quitar usuarios asociados y traer todos los componentes para obterner las dependencias|
||DocumentChecklistItem.DocumentApproval|||
||Quote.Approval_Commission|||
|Vlocity Document template|clbIns_ContractTemplate_V2||Crear manualmente|
||Policy|||
||SLIP AP 1|||
||SLIP AP 3|||
<br>
<br>

<!-- 11 -----------------------------------------------------LISTA DE COMPONENTES-------------------------------------------------------------------------- -->

## 11. Cargue de registros: Actividades Economica Riesgos

Luego de migrar el objeto ActividadEconomica__c, se procede con el cargue de los registros:


* A través de Dataloader se exportan los registros existentes en TA.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader12.png?raw=true" width=500>
	</p>  
		
* Se selecciona el objeto y la ruta en donde se almacena el CSV.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader1.png?raw=true" width=500>
	</p>  
	
* Se marcan todos los campos del objeto. 

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader2.png?raw=true" width=500>
	</p>  	
	
* Si el proceso no falla aparece la confirmación de registros exportados.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader3.png?raw=true" width=500>
	</p>  	

* 🚩 CSV registros del objeto , [Link](https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomica__c.csv)

* Por medio de Dataloader se insertan los registros en producción.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader4.png?raw=true" width=500>
	</p>  	

* CSV con el cual se puede realizar el insert del proceso, [Link](https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomica__c.csv)

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader5.png?raw=true" width=500>
	</p> 
	
* Aparece la confirmación de lectura del archivo CSV.	

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader6.png?raw=true" width=500>
	</p> 
	
* Se crea el mapeo de datos.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader7.png?raw=true" width=500>
	</p> 
	
* Ejecutamos el Auto - Match.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader8.png?raw=true" width=500>
	</p> 

* Luego de realizar el auto-match, quitamos la opción del OwnerId ya que el id que contiene el CSV es posible que no exista en el servidor de destino.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader9.png?raw=true" width=500>
	</p> 

* Finalizamos el proceso.

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader10.png?raw=true" width=500>
	</p> 
	
* Por último verificamos que los registros se hubiesen creado correctamente

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ActividadEconomicaDLoader11.png?raw=true" width" width=500>
	</p> 

Archivo con el listado de componentes , [Link](https://startupsfa-my.sharepoint.com/:x:/g/personal/cristiaam_cloudblue_us/EQLb96dv7opIqzVNHUlEU5sBV-JD4jv5RAqWjdUMWQZkkA?e=R5OTaz&nav=MTVfezY0M0JGMTA3LTA1NzQtNEVFQy1CMzE5LTQ0RTY2QzI3NDQzMn0)

<!-- 12 -----------------------------------------------------Permisos Perfiles-------------------------------------------------------------------------- -->

## 12. Perfiles

12.1	Permisos del Perfil x Objeto: 

* A continuación se encuentra la relación de permisos a nivel de Objetos por cada Perfil. Por favor recuerde que los objetos se pueden encontrar por el Api Name o por el Label, este último se puede encontrar en singular o en plural

 	| Diccionario de siglas |
	| --------------------- |
	| C : Create|  
	| R : Read|  
	| U : Update|  
	| D : Delete|  
	| V : View All|  
	| M : Modify All|


| Object (Api Name)                                        | Object (Label)                           | Profesional Comercial (Gerente) | Jefe Tecnico | Tecnico de operaciones |
| -------------------------------------------------------- | ---------------------------------------- | ------------------------------- | ------------ | ---------------------- |
| Account                                                  | Account                                  | CRUV                            | RUV          | RUV                    |
| ActionPlan                                               | Action Plan                              | CRUV                            | CRU          | CRU                    |
| ActionPlanTemplate                                       | Action Plan Template                     | CRUV                            | CRU          | CRU                    |
| ActividadEconomica__c                                    | Actividad Economica Riesgo               | R                               | R            | R                      |
| Address                                                  | Address                                  | CRUV                            | CRUV         | CRUV                   |
| AIRecordInsight                                          | AI Record Insight                        | RUV                             | RUV          | RUV                    |
| Asset                                                    | Asset                                    | CRU                             | CRUV         | CRUV                   |
| Asuntos__c                                               | Asunto                                   | CRUV                            | CRUV         | CRUV                   |
| AuthorizationForm                                        | Authorization Form                       | CRUV                            | CRUV         | CRUV                   |
| AuthorizationFormConsent                                 | Authorization Form Consent               | CRUV                            | CRUV         | CRUV                   |
| AuthorizationFormDataUse                                 | Authorization Form Data Use              | CRUV                            | CRUV         | CRUV                   |
| AuthorizationFormText                                    | Authorization Form Text                  | CRUV                            | CRUV         | CRUV                   |
| BusinessBrand                                            | Business Brand                           | CRUV                            | CRUV         | CRUV                   |
| BusinessLicense                                          | Business License                         |                                 |              | CRU                    |
| CalculationProcedure                                     | Calculation Procedure                    | RV                              | RV           | RV                     |
| CalculationProcedureVariable                             | Calculation Procedure Variable           | CRUV                            | CRUV         | CRUV                   |
| CalculationProcedureVersion                              | Calculation Procedure Version            | CRUV                            | CRUV         | CRUV                   |
| Campaign                                                 | Campaign                                 | CRUV                            | CRUV         | CRUV                   |
| Capacitacion__c                                          | Capacitación                             | CRUV                            | CRUV         | CRUV                   |
| Case                                                     | Case                                     | CRU                             | CRUV         | CRUV                   |
| ChannelProgram                                           | Channel Program                          | RV                              | CRUV         | CRUV                   |
| ChannelProgramLevel                                      | Channel Program Level                    | CRUV                            | CRUV         | CRUV                   |
| ChannelProgramMember                                     | Channel Program Member                   | CRU                             | CRU          | CRU                    |
| Ciudades__c                                              | Ciudad                                   | RV                              | CRUV         | CRUV                   |
| Claim                                                    | Claim                                    | RV                              | RV           | RV                     |
| ClaimCase                                                | Claim Case                               |                                 | CRUV         | CRUV                   |
| ClaimCoverage                                            | Claim Coverage                           | RV                              | CRUV         | CRUV                   |
| ClaimCoveragePaymentDetail                               | Claim Coverage Payment Detail            | CRUV                            | CRUV         | CRUV                   |
| ClaimCovPaymentAdjustment                                | Claim Coverage Payment Adjustment        | CRV                             | CRUV         | CRUV                   |
| ClaimCovReserveAdjustment                                | Claim Coverage Reserve Adjustment        | CRUV                            | CRUV         | CRUV                   |
| ClaimParticipant                                         | Claim Participant                        |                                 | CRUV         | CRUV                   |
| ClaimPaymentSummary                                      | Claim Payment Summary                    |                                 | CRUV         | CRUV                   |
| Colaborador_por_campana__c                               | Asesor asignado                          | CRU                             | R            | R                      |
| comentarios_de_incidencia__c                             | Comentarios de Incidencia                | RV                              | CRUV         | CRUV                   |
| CommissionSchedule                                       | Commission Schedule                      | CRUV                            | CRUV         | CRUV                   |
| CommSubscription                                         | Communication Subscription               | CRUV                            | CRUV         | CRUV                   |
| CommSubscriptionChannelType                              | Communication Subscription Channel Type  | CRUV                            | CRUV         | CRUV                   |
| CommSubscriptionConsent                                  | Communication Subscription Consent       | CRUV                            | CRUV         | CRUV                   |
| CommSubscriptionTiming                                   | Communication Subscription Timing        | CRUV                            | CRUV         | CRUV                   |
| Contact                                                  | Contact                                  | CRU                             | CRU          | CRU                    |
| Contacto_principal__c                                    | Contacto principal                       | CRUV                            | CRUV         | CRUV                   |
| ContactPointAddress                                      | Contact Point Address                    | RV                              | CRUV         | CRUV                   |
| ContactPointConsent                                      | Contact Point Consent                    |                                 | CRUV         | CRUV                   |
| ContactPointEmail                                        | Contact Point Email                      |                                 | CRUV         | CRUV                   |
| ContactPointPhone                                        | Contact Point Phone                      |                                 | CRUV         | CRUV                   |
| ContactPointTypeConsent                                  | Contact Point Type Consent               |                                 | CRUV         | CRUV                   |
| ContactRequest                                           | Contact Request                          |                                 | CRUV         | CRUV                   |
| Contract                                                 | Contract                                 | CRUV                            | CRUV         | CRUV                   |
| ContractGroupPlan                                        | Contract Group Plan                      |                                 | CRU          | CRUDVM                 |
| ContractGroupPlanGroupClass                              | Contract Group Plan Group Class          |                                 |              | CRUDVM                 |
| cookiecon__Cookie__c                                     | Cookie                                   | CRUD                            |              |                        |
| cookiecon__CookieConsent__c                              | Cookie Consent                           | CRUD                            |              |                        |
| cookiecon__CookieConsentCategory__c                      | Cookie Consent Category                  | CRUD                            |              |                        |
| CoverageType                                             | Coverage Type                            |                                 | CRUV         | CRUV                   |
| Customer                                                 | Customer                                 | CRUV                            | CRUV         | CRUV                   |
| CustomerProperty                                         | Customer Property                        | CRUV                            | CRU          | CRU                    |
| DataUseLegalBasis                                        | Data Use Legal Basis                     | CRUV                            | CRUV         | CRUV                   |
| DataUsePurpose                                           | Data Use Purpose                         | CRUV                            | CRUV         | CRUV                   |
| DatosContactoComercial__c                                | Datos Contacto Comercial                 | CRUV                            | CRUV         | CRUV                   |
| Digital__c                                               | Digital                                  | CRUV                            | CRUV         | CRUV                   |
| DistributorAuthorization                                 | Distributor Authorization                | CRUV                            | CRUV         | CRUV                   |
| Document                                                 | Document                                 | CRU                             | CRU          | CRU                    |
| DocumentChecklistItem                                    | Document Checklist Item                  | CRUV                            | CRUV         | CRUV                   |
| DocumentClause                                           | Document Clause                          | CRU                             | CRU          | CRU                    |
| DocumentEnvelope                                         | Document Envelope                        | CRUV                            | CRUV         | CRUV                   |
| DocumentGenerationProcess                                | Document Generation Process              | CRUV                            | CRUV         | CRUV                   |
| DocumentRecipient                                        | Document Recipient                       | CRUV                            | CRUV         | CRUV                   |
| DocumentTemplate                                         | Document Template                        | CRUV                            | CRUV         | CRU                    |
| DuplicateRecordSet                                       | Duplicate Record Set                     | RV                              | RV           | RV                     |
| EngagementChannelType                                    | Engagement Channel Type                  | CRUV                            | CRUV         | CRUV                   |
| Estrategia_Comercial__c                                  | Estrategia Comercial                     | CRU                             | CRUV         | CRUV                   |
| EvaluacionSeguimiento__c                                 | Evaluación Seguimiento                   | CRU                             | CRUV         | CRUV                   |
| ExpressionSet                                            | Expression Set                           | RV                              | RV           | RV                     |
| FinancialDeal                                            | Financial Deal                           | CRUV                            | CRUV         | CRUV                   |
| FinancialDealAsset                                       | Financial Deal Asset                     | CRUV                            | CRUV         | CRUV                   |
| FinancialDealBid                                         | Financial Deal Bid                       | CRUV                            | CRUV         | CRUV                   |
| FinancialDealParty                                       | Financial Deal Party                     | CRUV                            | CRUV         | CRUV                   |
| FinancialDealProduct                                     | Financial Deal Product                   | CRUV                            | CRUV         | CRUV                   |
| FinServ__AccountAccountRelation__c                       | Account-Account Relationship             | CRUDV                           | CRUV         | CRU                    |
| FinServ__Alert__c                                        | Alert                                    | CRUD                            | R            | R                      |
| FinServ__AssetsAndLiabilities__c                         | Assets and Liabilities                   | CRUD                            | R            | R                      |
| FinServ__BillingStatement__c                             | Billing Statement                        | CRUD                            |              |                        |
| FinServ__Card__c                                         | Card                                     | CRUD                            | CRU          | R                      |
| FinServ__ChargesAndFees__c                               | Charges And Fees                         | CRUD                            | CRU          | CRU                    |
| FinServ__ContactContactRelation__c                       | Contact-Contact Relationship             | CRUD                            | R            | R                      |
| FinServ__Education__c                                    | Education                                | CRUD                            | R            | R                      |
| FinServ__Employment__c                                   | Employment                               | CRUD                            | R            | R                      |
| FinServ__FinancialAccount__c                             | Financial Account                        | CRUD                            | RV           | RV                     |
| FinServ__FinancialAccountRole__c                         | Financial Account Role                   | CRUD                            | RV           | RV                     |
| FinServ__FinancialAccountTransaction__c                  | Financial Account Transaction            | CRUD                            | RV           | RV                     |
| FinServ__FinancialGoal__c                                | Financial Goal                           | CRUD                            | RV           | RV                     |
| FinServ__FinancialHolding__c                             | Financial Holding                        | CRUD                            | RV           | RV                     |
| FinServ__IdentificationDocument__c                       | Identification Document                  | CRUD                            | R            | R                      |
| FinServ__LifeEvent__c                                    | Life Event                               | CRUD                            | R            | R                      |
| FinServ__PolicyPaymentMethod__c                          | Policy Payment Method                    | CRUD                            | R            | R                      |
| FinServ__ReciprocalRole__c                               | Reciprocal Role                          | CRUD                            |              |                        |
| FinServ__Revenue__c                                      | Revenue                                  | CRUD                            | R            | R                      |
| FinServ__RollupByLookupConfig__c                         | Rollup By Lookup Configuration           | CRUD                            | R            | R                      |
| FinServ__RollupByLookupFilterCriteria__c                 | Rollup By Lookup Filter Criteria         | CRUD                            | R            | R                      |
| FinServ__Securities__c                                   | Securities                               | CRUD                            | R            | R                      |
| FSCTransition__Assessment__c                             | Assessment                               | CRUD                            | R            | R                      |
| FSCTransition__AsyncRequest__c                           | Async Request                            | CRUD                            | R            | R                      |
| FSCTransition__System_Log__c                             | System Log                               | CRUD                            |              |                        |
| FSCTransition__System_Log_Event__e                       | System Log Event                         | CR                              | CR           | CR                     |
| GeneralParameters__c                                     | GeneralParameter                         | RU                              | RU           | RU                     |
| GeneratedDocument                                        | Generated Document                       | CRUV                            | CRUV         | CRUV                   |
| GroupCensus                                              | Group Census                             |                                 | CRU          | CRUDVM                 |
| GroupCensusMember                                        | Group Census Member                      |                                 | CRU          | CRUDVM                 |
| GroupCensusMemberPlan                                    | Group Census Member Plan                 |                                 | CRU          | CRUDVM                 |
| Idea                                                     | Idea                                     | CRU                             | CRU          | CRU                    |
| IdeaTheme                                                | Idea Theme                               | CRUV                            | CRUV         | CRUV                   |
| Idoneidad_Profesional__c                                 | Idoneidad Profesional                    | CRUV                            | CRUV         | CRUV                   |
| Incidencia__c                                            | Incidencia                               | CRU                             | CRUV         | CRUV                   |
| Individual                                               | Individual                               |                                 | CRUV         | CRUV                   |
| InsuranceContract                                        | Insurance Contract                       |                                 | CRU          | CRUDVM                 |
| InsurancePolicy                                          | Insurance Policy                         | CRU                             | CRU          | CRU                    |
| InsurancePolicyAsset                                     | Insurance Policy Asset                   |                                 | CRU          | CRU                    |
| InsurancePolicyCoverage                                  | Insurance Policy Coverage                |                                 | CRU          | CRU                    |
| InsurancePolicyMemberAsset                               | Insurance Policy Member Asset            |                                 | CRU          | CRU                    |
| InsurancePolicyParticipant                               | Insurance Policy Participant             |                                 | CRU          | CRU                    |
| InsuranceProfile                                         | Insurance Profile                        | CRU                             | CRU          | CRU                    |
| Interaction                                              | Interaction                              | RV                              | RV           | RV                     |
| InteractionSummary                                       | Interaction Summary                      | RV                              | RV           | RV                     |
| Lead                                                     | Lead                                     | CRU                             | CRU          | CRU                    |
| LegalEntity                                              | Legal Entity                             | CRUV                            | CRUV         | CRUV                   |
| LoanApplicant                                            | Loan Applicant                           | CRUV                            | CRUV         | CRUV                   |
| LoanApplicantAddress                                     | Loan Applicant Address                   | CRUV                            | CRUV         | CRUV                   |
| LoanApplicantDeclaration                                 | Loan Applicant Declaration               | CRUV                            | CRUV         | CRUV                   |
| LoanApplicantEmployment                                  | Loan Applicant Employment                | CRUV                            | CRUV         | CRUV                   |
| LoanApplicantIncome                                      | Loan Applicant Income                    | CRUV                            | CRUV         | CRUV                   |
| LoanApplicationAsset                                     | Loan Application Asset                   | CRUV                            | CRUV         | CRUV                   |
| LoanApplicationFinancial                                 | Loan Application Financial               | CRUV                            | CRUV         | CRUV                   |
| LoanApplicationLiability                                 | Loan Application Liability               | CRUV                            | CRUV         | CRUV                   |
| LoanApplicationProperty                                  | Loan Application Property                | CRUV                            | CRUV         | CRUV                   |
| LoanApplicationTitleHolder                               | Loan Application Title Holder            | CRUV                            | CRUV         | CRUV                   |
| Location                                                 | Location                                 | CRUV                            | CRUV         | CRUV                   |
| LocationTrustMeasure                                     | Location Trust Measure                   | CRUV                            | CRUV         | CRUV                   |
| ltngsharing__PrivateTestObject__c                        | PrivateTestObject                        | CRUD                            |              |                        |
| ltngsharing__ReadOnlyTestObject__c                       | ReadOnlyTestObject                       | CRUD                            | R            | R                      |
| Macro                                                    | Macro                                    | CRUV                            | CRUV         | CRUV                   |
| Materiales__c                                            | Material                                 | CRUV                            | CRUV         | CRUV                   |
| Materiales_x_Campanas__c                                 | Material x Campaña                       | CRU                             | CRUV         | CRUV                   |
| OmniDataPack                                             | Omni DataPack                            | CRUV                            | CRUV         | CRUV                   |
| OmniDataTransform                                        | Omni Data Transformation                 | CRUV                            | CRUV         | CRUV                   |
| OmniDataTransformConfig                                  | Omni Data Transformation Config          | CRUV                            | CRUV         | CRUV                   |
| OmniDataTransformItem                                    | Omni Data Transformation Item            | CRUV                            | CRUV         | CRUV                   |
| OmniESignatureTemplate                                   | Omni Electronic Signature Template       | CRUV                            | CRUV         | CRUV                   |
| OmniIntegrationProcConfig                                | Omni Integration Procedure Configuration | CRUV                            | CRUV         | CRUV                   |
| OmniInteractionAccessConfig                              | Omni Interaction Access Configuration    | CRUV                            | CRUV         | CRUV                   |
| OmniInteractionConfig                                    | Omni Interaction Configuration           | CRUV                            | CRUV         | CRUV                   |
| OmniProcess                                              | Omni Process                             | CRUV                            | CRUV         | CRUV                   |
| OmniProcessCompilation                                   | Omni Process Compilation                 | CRUV                            | CRUV         | CRUV                   |
| OmniProcessElement                                       | Omni Process Element                     | CRUV                            | CRUV         | CRUV                   |
| OmniProcessTransientData                                 | Omni Process Transient Data              | CRUV                            | CRUV         | CRUV                   |
| OmniScriptConfig                                         | Omni Script Configuration                | CRUV                            | CRUV         | CRUV                   |
| OmniScriptSavedSession                                   | OmniScript Saved Session                 | CRUV                            | CRUV         | CRUV                   |
| OmniUiCard                                               | Omni UI Card                             | CRUV                            | CRUV         | CRUV                   |
| OmniUiCardConfig                                         | Omni Ui Card Config                      | CRUV                            | CRUV         | CRUV                   |
| Opportunity                                              | Opportunity                              | CRUV                            | CRUV         | CRV                    |
| Order                                                    | Order                                    | CRUV                            | CRUV         | CRUV                   |
| Parametros__c                                            | Parámetro                                | CRUV                            | CRUV         | CRUV                   |
| PartnerFundAllocation                                    | Partner Fund Allocation                  | CRUV                            | CRUV         | CRUV                   |
| PartnerFundClaim                                         | Partner Fund Claim                       | CRUV                            | CRUV         | CRUV                   |
| PartnerFundRequest                                       | Partner Fund Request                     | CRUV                            | CRUV         | CRUV                   |
| PartnerMarketingBudget                                   | Partner Marketing Budget                 | CRUV                            | CRUV         | CRUV                   |
| PartyConsent                                             | Party Consent                            |                                 | CRUV         | CRUV                   |
| Plan_de_Entrenamiento__c                                 | Plan de Entrenamiento                    | CRU                             | CRUV         | CRUV                   |
| PlanAccion__c                                            | Plan de Acción                           | CRU                             | R            | CRU                    |
| Poliza__c                                                | Póliza/Plan                              | CRUV                            | CRUV         | CRUV                   |
| Pricebook2                                               | Price Book                               | RU                              | RU           | CRU                    |
| Producer                                                 | Producer                                 | CRUV                            | RUV          | CRUV                   |
| ProducerCommission                                       | Producer Commission                      | CRUV                            | CRUV         | CRUV                   |
| ProducerPolicyAssignment                                 | Producer Policy Assignment               |                                 |              | CRU                    |
| Product2                                                 | Product                                  | R                               | R            | R                      |
| PushTopic                                                | Push Topic                               | R                               | R            | R                      |
| QuickText                                                | Quick Text                               | CRUV                            | CRUV         | CRUV                   |
| Quote                                                    | Quote                                    | CRUDV                           | CRUDVM       | CRUDVM                 |
| QuoteLineItemGroupClass                                  | Quote Line Item Group Class              | CRU                             | CRU          | CRUV                   |
| ResidentialLoanApplication                               | Residential Loan Application             | CRUV                            | CRUV         | CRUV                   |
| SecuritiesHolding                                        | Securities Holding                       | CRUV                            | CRUV         | CRUV                   |
| Seller                                                   | Seller                                   | CRUV                            | CRUV         | CRUV                   |
| sf_devops__Branch__c                                     | Branch                                   | CRUV                            | CRUV         | CRUV                   |
| sf_devops__Change_Submission__c                          | Change Submission                        |                                 |              | R                      |
| sf_devops__Repository__c                                 | Repository                               |                                 |              | R                      |
| sf_devops__Submit_Component__c                           | Submit Component                         |                                 |              | R                      |
| SocialPost                                               | Social Post                              | CRUDV                           | CRUDV        | CRUV                   |
| Solution                                                 | Solution                                 | CRUV                            | CRUV         | CRUV                   |
| StreamingChannel                                         | Streaming Channel                        | CRUV                            | CRUV         | CRUV                   |
| TIMBASURVEYS__AnswerOption__c                            | AnswerOption                             | CRUD                            | CRUV         | CRUV                   |
| TIMBASURVEYS__Branches__c                                | Branch                                   | CRUDV                           |              | CRUV                   |
| TIMBASURVEYS__EmailSenderJob__c                          | EmailSenderJob                           | CRUD                            | R            | R                      |
| TIMBASURVEYS__Log__c                                     | Log                                      | CRUD                            | R            | R                      |
| TIMBASURVEYS__OptionBranchingRule__c                     | OptionBranchingRule                      | CRUDV                           |              | CRUV                   |
| TIMBASURVEYS__PageBranchingRule__c                       | PageBranchingRule                        | CRUDV                           |              | CRUV                   |
| TIMBASURVEYS__Picklist__c                                | Picklist                                 | CRUD                            | R            | R                      |
| TIMBASURVEYS__Question_Image__c                          | Question Image                           | CRUDV                           | CRUV         | CRUV                   |
| TIMBASURVEYS__Question_Summary__c                        | Question Summary                         | CRUD                            |              |                        |
| TIMBASURVEYS__QuestionBranchingRule__c                   | QuestionBranchingRule                    | CRUDV                           |              | CRUV                   |
| TIMBASURVEYS__QuestionToField__c                         | QuestionToField                          | CRUDV                           | CRUV         | CRUV                   |
| TIMBASURVEYS__QuestionType__c                            | SurveyStats                              | CRUDVM                          | R            | R                      |
| TIMBASURVEYS__Recipient__c                               | Recipient                                | CRUDV                           | CRUV         | CRUV                   |
| TIMBASURVEYS__Survey__c                                  | Survey                                   | CRUV                            | R            | R                      |
| TIMBASURVEYS__Survey_Summary__c                          | Survey Summary                           | CRUDVM                          | R            | R                      |
| TIMBASURVEYS__SurveyPage__c                              | SurveyPage                               | CRUV                            | R            | R                      |
| TIMBASURVEYS__SurveyQuestion__c                          | SurveyQuestion                           | CRUDVM                          | CRUV         | CRUV                   |
| TIMBASURVEYS__SurveyRelationship__c                      | SurveyRelationship                       | CRUDVM                          | R            | R                      |
| TIMBASURVEYS__SurveyResponse__c                          | SurveyResponse                           | CRUDVM                          | R            | R                      |
| TIMBASURVEYS__SurveyTheme__c                             | SurveyTheme                              | CRUDVM                          | R            | R                      |
| TIMBASURVEYS__TimbaSurveyData__c                         | TimbaSurveyData                          | CRUV                            | CRUV         | CRUV                   |
| Ubicacion__c                                             | Ubicacion                                | R                               | R            | R                      |
| UpgradePlan__c                                           | Upgrade Plan                             |                                 |              | R                      |
| UpgradeStep__c                                           | Upgrade Step                             |                                 |              | R                      |
| UserEsignVendorIdentifier                                | User Esignature Vendor Identifier        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__AccountAppliedPromotion__c                  | Applied Promotion                        | CRUD                            | R            | R                      |
| vlocity_ins__AccountAppliedPromotionItem__c              | Applied Promotion Affected Asset         | CRUD                            | R            | R                      |
| vlocity_ins__AccountPriceAdjustment__c                   | Account Pricing                          | CRUD                            | R            | R                      |
| vlocity_ins__AccountRegulatoryAction__c                  | Account Regulatory Action                | CRUD                            | R            | R                      |
| vlocity_ins__ActivityContentDocument__c                  | Activity Content Document                | CRUD                            | R            | R                      |
| vlocity_ins__ActivityTemplate__c                         | Activity Template                        | CRUD                            | R            | R                      |
| vlocity_ins__AdminTabLayout__c                           | Admin Tab Layout                         | CRUD                            | R            | R                      |
| vlocity_ins__AgencyAppointment__c                        | Agency/Brokerage Appointment             | CRUD                            | R            | R                      |
| vlocity_ins__AgencyLicense__c                            | Agency/Brokerage License                 | CRUD                            | R            | R                      |
| vlocity_ins__AgencyPayment__c                            | Agency/Brokerage Payment                 | CRUD                            | R            | R                      |
| vlocity_ins__Application__c                              | Application                              | CRUD                            | R            | R                      |
| vlocity_ins__ApplicationPartyRelationship__c             | Application Party Relationship           | CRUD                            |              |                        |
| vlocity_ins__ApplicationTemplate__c                      | Application Template                     | CRUD                            | R            | R                      |
| vlocity_ins__Assessment__c                               | Assessment                               | CRUD                            | R            | R                      |
| vlocity_ins__AssessmentAnswer__c                         | Assessment Answer                        | CRUD                            | R            | R                      |
| vlocity_ins__AssessmentQuestion__c                       | Assessment Question                      | CRUD                            | R            | R                      |
| vlocity_ins__AssetCoverage__c                            | Policy Coverage                          | CRUD                            | R            | R                      |
| vlocity_ins__AssetInsuredItem__c                         | Insured Item                             | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__AssetPartyRelationship__c                   | Held Product Relationship                | CRUD                            | R            | R                      |
| vlocity_ins__AssetPricingAdjustment__c                   | Policy Pricing Adjustment                | CRUD                            | R            | R                      |
| vlocity_ins__AssetRevenueScheduleEntry__c                | Revenue Schedule Entry                   | CRUD                            | R            | R                      |
| vlocity_ins__AssetSecurityPosition__c                    | Security Position                        | CRUD                            | R            | R                      |
| vlocity_ins__AssetTerm__c                                | Policy Terms                             | CRUD                            | R            | R                      |
| vlocity_ins__AssetTermTrackingEntry__c                   | Policy Terms Tracking Entry              | CRUD                            | R            | R                      |
| vlocity_ins__AssetTransaction__c                         | Transaction                              | CRUD                            | R            | R                      |
| vlocity_ins__AssignmentRule__c                           | Manual Queue Assignment Rule             | CRUD                            | R            | R                      |
| vlocity_ins__Attribute__c                                | Vlocity Attribute                        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__AttributeAssignment__c                      | Attribute Assignment                     | CRUD                            | R            | R                      |
| vlocity_ins__AttributeAssignmentExport__c                | Attribute Assignment Export              | CRUD                            | R            | R                      |
| vlocity_ins__AttributeAssignmentRule__c                  | Vlocity Attribute Assignment Rule        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__AttributeBinding__c                         | Vlocity Attribute Binding                | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__AttributeCategory__c                        | Vlocity Attribute Category               | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__BillingAccount__c                           | Billing Account                          | CRUD                            | CRU          | CRU                    |
| vlocity_ins__BusinessSite__c                             | Site                                     | CRUD                            | R            | R                      |
| vlocity_ins__BusinessSiteOffering__c                     | Site Offering                            | CRUD                            | R            | R                      |
| vlocity_ins__CachedAPIResponse__c                        | CachedAPIResponse                        | CRUD                            |              |                        |
| vlocity_ins__CachedDataSet__c                            | Cached Data Set                          | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__CachedFilterableAttribute__c                | Cached Filterable Attribute              | CRUD                            | CRU          | CRUV                   |
| vlocity_ins__CachedPriceBookEntryAttributeValue__c       | Cached PriceBookEntry Attribute Value    | CRUD                            | R            | R                      |
| vlocity_ins__CachedProduct2Translation__c                | Cached Product Translation               | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__CachedPromotionTranslation__c               | Cached Promotion Translation             | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationMatrix__c                        | Vlocity Calculation Matrix               | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationMatrixColumn__c                  | Vlocity Calculation Matrix Column        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationMatrixDimension__c               | Vlocity Calculation Matrix Dimension     | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationMatrixRow__c                     | Vlocity Calculation Matrix Row           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationMatrixVersion__c                 | Vlocity Calculation Matrix Version       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationProcedure__c                     | Vlocity Calculation Procedure            | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationProcedureStep__c                 | Vlocity Calculation Procedure Step       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationProcedureVariable__c             | Vlocity Calculation Procedure Variable   | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CalculationProcedureVersion__c              | Vlocity Calculation Procedure Version    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__CallbackURI__c                              | CallbackURI                              | CRUD                            |              |                        |
| vlocity_ins__CampaignContentDocument__c                  | Campaign Content Document                | CRUD                            |              |                        |
| vlocity_ins__CampaignMemberActionLog__c                  | Campaign Member Action Log               | CRUD                            |              |                        |
| vlocity_ins__Catalog__c                                  | Catalog                                  | CRUD                            |              |                        |
| vlocity_ins__CatalogProductRelationship__c               | Catalog Product Relationship             | CRUD                            |              |                        |
| vlocity_ins__CatalogRelationship__c                      | Catalog Relationship                     | CRUD                            |              |                        |
| vlocity_ins__ChargeMeasurement__c                        | Charge Measurement                       | CRUD                            | CRU          | R                      |
| vlocity_ins__ClaimantEarning__c                          | Claimant Earning                         | CRUD                            | R            | R                      |
| vlocity_ins__ClaimCertificateOfCapacity__c               | Claim Certificate Of Capacity            | CRUD                            | CRU          | CRU                    |
| vlocity_ins__ClaimCoverage__c                            | Claim Coverage                           | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__ClaimLineItem__c                            | Claim Line Item                          | CRUD                            |              |                        |
| vlocity_ins__ClaimPayment__c                             | Claim Payment                            | CRUD                            |              |                        |
| vlocity_ins__CompiledAttributeOverride__c                | Compiled Attribute Override              | CRUD                            |              |                        |
| vlocity_ins__ConsoleActionLog__c                         | Console Action Log                       | CRUD                            |              |                        |
| vlocity_ins__ConsumerDrug__c                             | Medication                               | CRUD                            | CRU          | CRU                    |
| vlocity_ins__ConsumerProvider__c                         | Consumer Provider                        | CRUD                            |              |                        |
| vlocity_ins__ContactEmployment__c                        | Contact Employment                       | CRUD                            | R            | R                      |
| vlocity_ins__ContactRegulatoryAction__c                  | Contact Regulatory Action                | CRUD                            |              |                        |
| vlocity_ins__ContextAction__c                            | Context Action                           | CRUD                            |              |                        |
| vlocity_ins__ContextDimension__c                         | Vlocity Context Dimension                | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ContextMapping__c                           | Vlocity Context Mapping                  | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ContextMappingArgument__c                   | Vlocity Context Mapping Argument         | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ContextRule__c                              | Vlocity Context Rule                     | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ContextRuleset__c                           | Vlocity Context Ruleset                  | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ContextScope__c                             | Context Scope                            | CRUD                            |              |                        |
| vlocity_ins__ContractDocumentCollection__c               | Contract Document Element                | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractEnvelope__c                         | Contract Document Envelope               | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractGroup__c                            | Contract Group                           | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractLineItem__c                         | Plan                                     | CRUDV                           | R            | CRU                    |
| vlocity_ins__ContractProviderNetwork__c                  | Contract Provider Network                | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractRecipient__c                        | Contract Recipient                       | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractSection__c                          | Contract Document Section                | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractTerm__c                             | Contract Term                            | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractType__c                             | Contract Type                            | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractTypeSetting__c                      | Contract Type Setting                    | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractTypeTerm__c                         | Contract Type Term                       | CRUD                            | R            | CRU                    |
| vlocity_ins__ContractVersion__c                          | Contract Document                        | CRUD                            | CRU          | CRU                    |
| vlocity_ins__CustomerInteraction__c                      | Customer Interaction                     | CRUD                            | R            | R                      |
| vlocity_ins__CustomerInteractionTopic__c                 | Customer Interaction Topic               | CRUD                            | R            | R                      |
| vlocity_ins__Datastore__c                                | Vlocity Data Store                       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__DecompositionRelationship__c                | Decomposition Relationship               | CRUD                            |              |                        |
| vlocity_ins__DiagnosisToProcedureCodeMapping__c          | Diagnosis To Procedure Code Mapping      | CRUD                            |              |                        |
| vlocity_ins__Document__c                                 | Document                                 | CRUDV                           | CRUV         | CRUV                   |
| vlocity_ins__DocumentClause__c                           | Document Clause                          | CRUD                            | RU           | RU                     |
| vlocity_ins__DocumentClauseCondition__c                  | Document Clause Condition                | CRUD                            | RU           | RU                     |
| vlocity_ins__DocumentSection__c                          | Document Section                         | CRUD                            | RU           | RU                     |
| vlocity_ins__DocumentTemplate__c                         | Document Template                        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__DocumentTemplateElement__c                  | Document Template Element                | CRUD                            | R            | R                      |
| vlocity_ins__DocumentTemplateSection__c                  | Document Template Section                | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__DocumentTemplateSectionCondition__c         | Document Template Section Condition      | CRUD                            |              |                        |
| vlocity_ins__DocumentToken__c                            | Document Token                           | CRUD                            | RU           | RU                     |
| vlocity_ins__DRBatchQueue__c                             | Vlocity DataRaptor Batch Queue           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__DRBulkData__c                               | DataRaptor Bulk Data                     | CRUD                            | R            | R                      |
| vlocity_ins__DRBundle__c                                 | Vlocity DataRaptor Bundle                | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__DRMapItem__c                                | Vlocity DataRaptor Map Item              | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Drug__c                                     | Drug                                     | CRUD                            | RU           | RU                     |
| vlocity_ins__DrugInteraction__c                          | Drug Interaction                         | CRUD                            | RU           | RU                     |
| vlocity_ins__DrugSubstitute__c                           | Drug Substitute                          | CRUD                            | RU           | RU                     |
| vlocity_ins__Element__c                                  | Vlocity OmniScript Element               | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__EntityFilter__c                             | Vlocity Entity Filter                    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__EntityFilterCondition__c                    | Vlocity Entity Filter Condition          | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__EntityFilterConditionArgument__c            | Vlocity Entity Filter Condition Argument | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__EntityFilterMember__c                       | Vlocity Entity Filter Member             | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ErrorCode__c                                | Error Code                               | CRUD                            | R            | R                      |
| vlocity_ins__ErrorCodeNamespace__c                       | Error Code Namespace                     | CRUD                            | R            | R                      |
| vlocity_ins__EventDuringInteraction__c                   | Event During Interaction                 | CRUD                            |              |                        |
| vlocity_ins__EventMessage__c                             | Vlocity Event Message                    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ExpandedInteractionLog__c                   | Expanded Interaction Log                 | CRUD                            |              |                        |
| vlocity_ins__FeeSchedule__c                              | Fee Schedule                             | CRUD                            |              |                        |
| vlocity_ins__FeeScheduleEntry__c                         | Fee Schedule Entry                       | CRUD                            |              |                        |
| vlocity_ins__FinancialAccount__c                         | Financial Account                        | CRUD                            | RV           | RV                     |
| vlocity_ins__FinancialAccountPartyRelationship__c        | Financial Account Party Relationship     | CRUD                            |              | R                      |
| vlocity_ins__FinancialSecurity__c                        | Security                                 | CRUD                            | R            | R                      |
| vlocity_ins__FinancialSecurityPosition__c                | Financial Account Security Position      | CRUD                            | RV           | RV                     |
| vlocity_ins__FinancialStatement__c                       | Financial Statement                      | CRUD                            | RV           | RV                     |
| vlocity_ins__FinancialStatementLineItem__c               | Financial Statement Line Item            | CRUD                            | RV           | RV                     |
| vlocity_ins__Formulary__c                                | Formulary                                | CRUD                            | R            | R                      |
| vlocity_ins__FormularyDrug__c                            | Formulary Drug                           | CRUD                            | R            | R                      |
| vlocity_ins__FormularyDrugStepTherapy__c                 | Formulary Drug Step Therapy              | CRUD                            | R            | R                      |
| vlocity_ins__FormularyTier__c                            | Formulary Tier                           | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentDiagram__c                        | Fulfilment Diagram                       | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentDiagramOPD__c                     | Fulfilment Diagram OPD                   | CRUD                            |              |                        |
| vlocity_ins__FulfilmentRequest__c                        | Fulfilment Request                       | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentRequestDecompRelationship__c      | Fulfilment Request Decomposition Rel     | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentRequestLine__c                    | Fulfilment Request Line                  | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentRequestLineDecompRelationship__c  | FulfilmentRequestLineDecompRelationship  | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentRequestLineRelationship__c        | FulfilmentRequestLineRelationship        | CRUD                            | R            | R                      |
| vlocity_ins__FulfilmentRequestLineSourceRootOrderItem__c | FRL Source Bundle Relationship           | CRUD                            | R            | R                      |
| vlocity_ins__GenericDocument__c                          | Generic DocuSign Document                | CRUD                            |              |                        |
| vlocity_ins__GenericEnvelope__c                          | Generic DocuSign Envelope                | CRUD                            |              |                        |
| vlocity_ins__GenericRecipient__c                         | Generic DocuSign Recipient               | CRUD                            |              |                        |
| vlocity_ins__GraphClone__c                               | Graph Clone                              | CRUD                            | CRU          | CRU                    |
| vlocity_ins__GroupCensus__c                              | Census                                   | CRUD                            | CRU          | CRU                    |
| vlocity_ins__GroupCensusMember__c                        | Census Member                            | CRUD                            | CRU          | CRU                    |
| vlocity_ins__GroupCensusMemberPlan__c                    | Group Census Member Plan                 | CRUD                            | CRU          | CRUV                   |
| vlocity_ins__GroupClass__c                               | Group Class                              | CRUD                            | CRU          | CRU                    |
| vlocity_ins__GroupClassContribution__c                   | Group Class Contribution                 | CRUD                            | R            | R                      |
| vlocity_ins__Household__c                                | Household                                | CRUD                            | R            | R                      |
| vlocity_ins__InboundRESTInterface__c                     | Inbound REST Interface                   | CRUD                            | CRU          | CRU                    |
| vlocity_ins__InsClaimReserveTransaction__c               | Reserve Transaction                      | CRUD                            | R            | R                      |
| vlocity_ins__InsurableItem__c                            | Insurable Item                           | CRUD                            | R            | R                      |
| vlocity_ins__InsuranceClaim__c                           | Claim                                    | CRUD                            | R            | R                      |
| vlocity_ins__InsuranceClaimInvoice__c                    | Claim Invoice                            | CRUD                            |              |                        |
| vlocity_ins__InsuranceClaimInvolvedInjury__c             | Involved Party                           | CRUD                            | R            | R                      |
| vlocity_ins__InsuranceClaimInvolvedProperty__c           | Involved Property                        | CRUD                            | R            | R                      |
| vlocity_ins__InsuranceClaimLitigation__c                 | Claim Litigation                         | CRUD                            |              |                        |
| vlocity_ins__InsuranceClaimPartyRelationship__c          | Claim Relationship                       | CRUD                            |              |                        |
| vlocity_ins__InsuranceClaimRecovery__c                   | Claim Recovery                           | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__InsuranceClaimReport__c                     | Claim Report                             | CRUD                            | R            | R                      |
| vlocity_ins__InsuranceNonHeldPolicy__c                   | Deprecated Non Held Policy               | CRUD                            |              |                        |
| vlocity_ins__InsuranceProgram__c                         | Public Health Insurance Program          | CRUD                            |              |                        |
| vlocity_ins__InsuredGroupCensus__c                       | Insured Group Census                     | CRUD                            | R            | R                      |
| vlocity_ins__InsuredGroupCensusMember__c                 | Insured Group Census Member              | CRUD                            | CRUV         | CRUV                   |
| vlocity_ins__InsuredItemCoverage__c                      | Coverage                                 | CRUD                            | R            | R                      |
| vlocity_ins__InsuredItemPartyRelationship__c             | Insured Item Party                       | CRUD                            | CRUV         | RV                     |
| vlocity_ins__IntegrationRetryPolicy__c                   | Integration Retry Policy                 | CRUD                            | CRUV         | RV                     |
| vlocity_ins__Interface_DRGeneric__c                      | Vlocity DataRaptor Object Interface      | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Interface_InsurancePolicy__c                | Interface Insurance Policy               | CRUD                            | R            | R                      |
| vlocity_ins__Interface_ProductAttribute__c               | Product Attribute Interface              | CRUD                            | R            | R                      |
| vlocity_ins__InterfaceImplementation__c                  | Interface Implementation                 | CRUD                            | CRUV         | RV                     |
| vlocity_ins__InterfaceImplementationDetail__c            | Interface Implementation Detail          | CRUD                            | R            | R                      |
| vlocity_ins__InventoryItem__c                            | Inventory Item                           | CRUD                            | R            | R                      |
| vlocity_ins__InventoryItemDecompositionRelationship__c   | Inventory Item DecompositionRelationship | CRUD                            | R            | R                      |
| vlocity_ins__ItemImplementation__c                       | Item Implementation                      | CRUD                            | R            | R                      |
| vlocity_ins__Jurisdiction__c                             | Jurisdiction                             | CRUD                            | R            | R                      |
| vlocity_ins__LineOfBusiness__c                           | Line of Business                         | CRUD                            | R            | R                      |
| vlocity_ins__ManualQueue__c                              | Manual Queue                             | CRUD                            | R            | R                      |
| vlocity_ins__ManualQueueMember__c                        | Manual Queue Member                      | CRUD                            | R            | R                      |
| vlocity_ins__MarketingEvent__c                           | Marketing Event                          | CRUD                            | R            | R                      |
| vlocity_ins__MarketingEventDetail__c                     | Marketing Event Detail                   | CRUD                            | R            | R                      |
| vlocity_ins__MarketingEventRegistration__c               | Marketing Event Registration             | CRUD                            | R            | R                      |
| vlocity_ins__MarketingMaterial__c                        | Marketing Material                       | CRUD                            | R            | R                      |
| vlocity_ins__MarketingMaterialTracking__c                | Marketing Material Tracking              | CRUD                            | R            | R                      |
| vlocity_ins__NonHeldLoss__c                              | Loss                                     | CRUD                            | R            | R                      |
| vlocity_ins__NonHeldPolicy__c                            | Non Held Policy                          | CRUD                            | R            | R                      |
| vlocity_ins__NonHeldProduct__c                           | Non-Held Product                         | CRUD                            | R            | R                      |
| vlocity_ins__ObjectAppliedResult__c                      | Object Applied Result                    | CRUD                            | R            | R                      |
| vlocity_ins__ObjectClass__c                              | Vlocity Object or Object Type            | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ObjectElement__c                            | Vlocity Object Section Element           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ObjectFacet__c                              | Vlocity Object Facet                     | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ObjectFieldAttribute__c                     | Vlocity Object Field Attribute           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ObjectLayout__c                             | Vlocity Object Layout                    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ObjectRuleAssignment__c                     | Vlocity Object Rule Assignment           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ObjectSection__c                            | Vlocity Object Section                   | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Occurrence__c                               | Occurrence                               | CRUD                            | R            | R                      |
| vlocity_ins__OfferingProcedure__c                        | Vlocity Offering Procedure               | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__OfferMigrationComponentMapping__c           | Offer Migration Component Mapping        | CRUD                            | R            | R                      |
| vlocity_ins__OfferMigrationPlan__c                       | Offer Migration Plan                     | CRUD                            | R            | R                      |
| vlocity_ins__OfferPricingComponent__c                    | Offer Pricing Component                  | CRUD                            | R            | R                      |
| vlocity_ins__OmniScript__c                               | Vlocity OmniScript                       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__OmniScriptDefinition__c                     | Vlocity OmniScript Compiled Definition   | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__OmniScriptInstance__c                       | Saved OmniScript                         | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__OmniUserSession__c                          | Omni User Session                        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__OperatingHours__c                           | Operating Hours                          | CRUD                            |              |                        |
| vlocity_ins__OperatingHoursEntry__c                      | Operating Hours and Exceptions           | CRUD                            |              |                        |
| vlocity_ins__OpportunityAppliedPromotion__c              | Opportunity Applied Promotion            | CRUD                            |              |                        |
| vlocity_ins__OpportunityAppliedPromotionItem__c          | Opportunity Applied Promotion Item       | CRUD                            |              |                        |
| vlocity_ins__OpportunityGroup__c                         | Opportunity Group                        | CRUD                            | R            | R                      |
| vlocity_ins__OpportunityLineItemRelationship__c          | Opportunity Product Relationship         | CRUD                            | R            | R                      |
| vlocity_ins__OpportunityPriceAdjustment__c               | Opportunity Pricing                      | CRUD                            | R            | R                      |
| vlocity_ins__OrchestrationDependency__c                  | Orchestration Dependency                 | CRUD                            |              |                        |
| vlocity_ins__OrchestrationDependencyDefinition__c        | Orchestration Dependency Definition      | CRUD                            |              |                        |
| vlocity_ins__OrchestrationEvent__e                       | OrchestrationEvent                       | CR                              | CR           | CR                     |
| vlocity_ins__OrchestrationItem__c                        | Orchestration Item                       | CRUD                            |              |                        |
| vlocity_ins__OrchestrationItemDefinition__c              | Orchestration Item Definition            | CRUD                            |              |                        |
| vlocity_ins__OrchestrationItemLog__b                     | Orchestration Item Log                   | CRD                             | CRD          | CRD                    |
| vlocity_ins__OrchestrationItemRelationship__c            | Orchestration Item Relationship          | CRUD                            |              |                        |
| vlocity_ins__OrchestrationItemSource__c                  | Orchestration Item Source                | CRUD                            |              |                        |
| vlocity_ins__OrchestrationPlan__c                        | Orchestration Plan                       | CRUD                            |              |                        |
| vlocity_ins__OrchestrationPlanDefinition__c              | Orchestration Plan Definition            | CRUD                            |              |                        |
| vlocity_ins__OrchestrationQueue__c                       | Orchestration Queue                      | CRUD                            |              |                        |
| vlocity_ins__OrchestrationQueueAssignmentRule__c         | Orchestration Queue Assignment Rule      | CRUD                            |              |                        |
| vlocity_ins__OrchestrationScenario__c                    | Orchestration Scenario                   | CRUD                            |              |                        |
| vlocity_ins__OrchestrationSchedulerImplementation__c     | Orchestration Scheduler Implementation   | CRUD                            |              |                        |
| vlocity_ins__OrderAppliedPromotion__c                    | Order Applied Promotion                  | R                               |              |                        |
| vlocity_ins__OrderAppliedPromotionItem__c                | Order Applied Promotion Affected Item    | CRUD                            |              |                        |
| vlocity_ins__OrderEventLogEntry__b                       | Order Event                              | CRD                             | CRD          | CRD                    |
| vlocity_ins__OrderUpdate__e                              | OrderUpdate                              | CR                              | CR           | CR                     |
| vlocity_ins__OutboundConfiguration__c                    | Vlocity Outbound Configuration           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__OverrideDefinition__c                       | Product Override Definition              | CRUD                            | R            | R                      |
| vlocity_ins__Party__c                                    | Party                                    | CRUD                            |              | R                      |
| vlocity_ins__PartyMergeRequest__c                        | Party Merge Request                      | CRUD                            | R            | R                      |
| vlocity_ins__PartyRelationship__c                        | Party Relationship                       | CRUD                            | R            | R                      |
| vlocity_ins__PartyRelationshipType__c                    | Vlocity Party Relationship Type          | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__PaymentMethod__c                            | Payment Method                           | CRUD                            | R            | R                      |
| vlocity_ins__Picklist__c                                 | Vlocity Picklist                         | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__PicklistSelectionEntry__c                   | Picklist Selection Entry                 | CRUD                            | R            | R                      |
| vlocity_ins__PicklistValue__c                            | Vlocity Picklist Value                   | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Policy__c                                   | Policy                                   | CRUD                            | CRU          | CRU                    |
| vlocity_ins__PolicyClaimRelationship__c                  | Policy Claim Relationship                | CRUD                            | R            | R                      |
| vlocity_ins__PolicyCreditSurcharge__c                    | Credit & Surcharge                       | CRUD                            | R            | R                      |
| vlocity_ins__PolicyLineItem__c                           | Insured Items & People                   | CRUD                            | CRUV         | RV                     |
| vlocity_ins__PolicyPartyRelationship__c                  | Policy Relationship                      | CRUD                            |              |                        |
| vlocity_ins__PolicyTransaction__c                        | Policy Transaction                       | CRUD                            | R            | R                      |
| vlocity_ins__PolicyWithdrawalSurrenderLoan__c            | Withdrawal, Surrender, & Loan            | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Premises__c                                 | Premises                                 | CRUD                            | R            | R                      |
| vlocity_ins__PriceList__c                                | Tax and Fee                              | CRUV                            | R            | R                      |
| vlocity_ins__PriceListEntry__c                           | Product Tax and Fee                      | CRUD                            |              |                        |
| vlocity_ins__PricingComponent__c                         | Pricing Component                        | CRUD                            | R            | R                      |
| vlocity_ins__PricingComponentRelationship__c             | Pricing Component Relationship           | CRUD                            | R            | R                      |
| vlocity_ins__PricingElement__c                           | Pricing Element                          | CRUD                            | R            | R                      |
| vlocity_ins__PricingPlan__c                              | Pricing Plan                             | CRUD                            | R            | R                      |
| vlocity_ins__PricingPlanStep__c                          | Pricing Plan Step                        | CRUD                            | R            | R                      |
| vlocity_ins__PricingVariable__c                          | Pricing Variable                         | CRUD                            | R            | R                      |
| vlocity_ins__PricingVariableBinding__c                   | Pricing Variable Binding                 | CRUD                            | R            | R                      |
| vlocity_ins__ProducerAppointment__c                      | Producer Appointment                     | CRUD                            | RU           | CRU                    |
| vlocity_ins__ProducerEducation__c                        | Continuing Education                     | CRUD                            |              |                        |
| vlocity_ins__ProducerLicense__c                          | Producer License                         | CRUD                            | RU           | CRU                    |
| vlocity_ins__ProducerPayment__c                          | Producer Payment                         | CRUD                            | RU           | CRU                    |
| vlocity_ins__ProductAttribXN__c                          | ProductAttribXN                          | CRUD                            | R            | R                      |
| vlocity_ins__ProductChildItem__c                         | Product Child Item                       | CRUD                            | R            | R                      |
| vlocity_ins__ProductConfigurationChangeLog__c            | Product Configuration Change Log         | CRUD                            |              |                        |
| vlocity_ins__ProductConfigurationProcedure__c            | Product Configuration Procedure          | CRUD                            | R            | R                      |
| vlocity_ins__ProductionCode__c                           | Production Code                          | CRUD                            | CRU          | CRU                    |
| vlocity_ins__ProductJurisdictionNetwork__c               | Product Jurisdiction Network             | CRUD                            | R            | R                      |
| vlocity_ins__ProductRelationship__c                      | Product Relationship                     | CRUD                            | R            | R                      |
| vlocity_ins__ProductRelationshipType__c                  | Product Relationship Type                | CRUD                            | R            | R                      |
| vlocity_ins__ProductRequirement__c                       | Product Requirement                      | CRUD                            | R            | R                      |
| vlocity_ins__ProductTemplate__c                          | Product Template                         | CRUD                            | R            | R                      |
| vlocity_ins__ProfilingSegment__c                         | Deprecated Profiling Segment             | CRUD                            |              |                        |
| vlocity_ins__ProfilingSegmentCategory__c                 | Deprecated Profiling Segment Category    | CRUD                            |              |                        |
| vlocity_ins__ProfSegAssignment__c                        | Deprecated Profiling Segment Assignment  | CRUD                            |              |                        |
| vlocity_ins__ProgramEnrollment__c                        | Program Enrollment                       | CRUD                            | R            | R                      |
| vlocity_ins__ProgramEnrollmentDetermination__c           | Enrollment Determination                 | CRUD                            |              |                        |
| vlocity_ins__ProgramEnrollmentMember__c                  | Program Enrollment Member                | CRUD                            |              |                        |
| vlocity_ins__ProgramOutcome__c                           | Outcome                                  | CRUD                            |              |                        |
| vlocity_ins__Project__c                                  | Project                                  | CRUD                            |              |                        |
| vlocity_ins__ProjectItem__c                              | Project Item                             | CRUD                            |              |                        |
| vlocity_ins__Promotion__c                                | Promotion                                | CRUD                            |              |                        |
| vlocity_ins__PromotionApplicableProduct__c               | Promotion Applicable Product             | CRUD                            |              |                        |
| vlocity_ins__PromotionIncludedProduct__c                 | Promotion Included Product               | CRUD                            |              |                        |
| vlocity_ins__PromotionItem__c                            | Promotion Item                           | CRUD                            |              |                        |
| vlocity_ins__PromotionPricingAlteration__c               | Promotion Pricing Alteration             | CRUD                            |              |                        |
| vlocity_ins__ProviderAccountLicense__c                   | Provider Account License                 | CRUD                            |              |                        |
| vlocity_ins__ProviderContactLicense__c                   | Provider Contact License                 | CRUD                            |              |                        |
| vlocity_ins__ProviderEducation__c                        | Provider Education                       | CRUD                            |              |                        |
| vlocity_ins__ProviderFeeSchedule__c                      | Provider Fee Schedule                    | CRUD                            |              |                        |
| vlocity_ins__ProviderFeeScheduleEntry__c                 | Provider Fee Schedule Entry              | CRUD                            |              |                        |
| vlocity_ins__ProviderNetwork__c                          | Provider Network                         | CRUD                            |              |                        |
| vlocity_ins__ProviderNetworkFormularyDrugPrice__c        | Provider Network Formulary Drug Price    | CRUD                            |              |                        |
| vlocity_ins__ProviderNetworkMember__c                    | Provider Network Member                  | CRUD                            |              |                        |
| vlocity_ins__ProviderNetworkTier__c                      | Provider Network Tier                    | CRUD                            |              |                        |
| vlocity_ins__ProviderTaxonomy__c                         | Provider Taxonomy                        | CRUD                            |              |                        |
| vlocity_ins__QuoteAppliedPromotion__c                    | Quote Applied Promotion                  | CRUD                            | R            | R                      |
| vlocity_ins__QuoteAppliedPromotionItem__c                | Quote Applied Promotion Affected Item    | CRUD                            | R            | R                      |
| vlocity_ins__QuoteGroup__c                               | Quote Group                              | CRUDV                           | R            | R                      |
| vlocity_ins__QuoteGroupClassContribution__c              | Quote Group Class Contribution           | CRUD                            | R            | R                      |
| vlocity_ins__QuoteItemRelationship__c                    | Quote Item Relationship                  | CRUD                            | R            | R                      |
| vlocity_ins__QuoteLineItemGroupClass__c                  | Quote Line Item Group Class              | CRUD                            | R            | CRUV                   |
| vlocity_ins__QuoteLineItemPricingAdjustment__c           | Quote Line Item Pricing Adjustment       | CRUD                            | R            | CRUV                   |
| vlocity_ins__QuoteLineItemRateBreakout__c                | Quoted Plan Rate Breakout                | CRUD                            | R            | R                      |
| vlocity_ins__QuoteLineItemRelationship__c                | Quote Product Relationship               | CRUD                            | R            | R                      |
| vlocity_ins__QuotePricingAdjustment__c                   | Quote Pricing Adjustment                 | CRUD                            | R            | RV                     |
| vlocity_ins__RateBand__c                                 | Rate Band                                | CRUD                            |              |                        |
| vlocity_ins__RateBandTier__c                             | Rate Band Tier                           | CRUD                            |              |                        |
| vlocity_ins__RelationshipGraph__c                        | Relationship Graph                       | CRUD                            |              |                        |
| vlocity_ins__RelationshipGraphNodeType__c                | Relationship Graph Node Type             | CRUD                            |              |                        |
| vlocity_ins__RelationshipGraphTraversal__c               | Relationship Graph Traversal             | CRUD                            |              |                        |
| vlocity_ins__Rule__c                                     | Vlocity Rule                             | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__RuleAction__c                               | Vlocity Rule Action                      | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__RuleAssignment__c                           | Vlocity Rule Assignment                  | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__RuleFilter__c                               | Vlocity Rule Filter                      | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__RuleProperty__c                             | Screening Rule Property                  | CRUD                            |              |                        |
| vlocity_ins__RuleVariable__c                             | Vlocity Rule Variable                    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__ScreeningRule__c                            | Screening Rule                           | CRUD                            | R            | R                      |
| vlocity_ins__ScreeningRuleGroup__c                       | Screening Rule Group                     | CRUD                            | CRU          | CRU                    |
| vlocity_ins__ServicePoint__c                             | Service Point                            | CRUD                            |              |                        |
| vlocity_ins__SICCode__c                                  | SIC Code                                 | CRUD                            | R            | R                      |
| vlocity_ins__Stage__c                                    | Vlocity DataRaptor Staged Data           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Statement__c                                | Statement                                | CRUD                            | R            | R                      |
| vlocity_ins__StateTransition__c                          | State Transition                         | CRUD                            | R            | R                      |
| vlocity_ins__String__c                                   | Vlocity String                           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__StringTranslation__c                        | Vlocity String Translation               | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__Subscription__c                             | Subscription                             | CRUD                            | R            | R                      |
| vlocity_ins__SyncDeltaObject__c                          | Sync Delta Object                        | CRUD                            | R            | R                      |
| vlocity_ins__SyncDeltaSnapshot__c                        | Sync Delta Snapshot                      | CRUD                            | R            | R                      |
| vlocity_ins__System__c                                   | System                                   | CRUD                            |              |                        |
| vlocity_ins__SystemInterface__c                          | System Interface                         | CRUD                            |              |                        |
| vlocity_ins__TestResult__c                               | Test Result                              | CRUD                            | R            | R                      |
| vlocity_ins__ThorOrchestrationQueue__c                   | Thor Orchestration Queue                 | CRUD                            |              |                        |
| vlocity_ins__TimePlan__c                                 | Time Plan                                | CRUD                            |              | R                      |
| vlocity_ins__TimePolicy__c                               | Time Policy                              | CRUD                            |              | R                      |
| vlocity_ins__TrailingDocumentPlaceholder__c              | Trailing Document Placeholder            | CRUD                            | R            | R                      |
| vlocity_ins__UiFacet__c                                  | Vlocity UI Facet                         | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__UiSection__c                                | Vlocity UI Section                       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__UserCalendar__c                             | User Calendar                            | CRUD                            | CRU          | CRU                    |
| vlocity_ins__UserNotification__c                         | Notification                             | CRUD                            | CRUV         | CRV                    |
| vlocity_ins__Venue__c                                    | Venue                                    | CRUD                            | CRU          | CRU                    |
| vlocity_ins__VlocityAction__c                            | Vlocity Action                           | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityAPIMetadata__c                       | Vlocity API Metadata                     | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityAttachment__c                        | Vlocity Attachment                       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityCard__c                              | Vlocity Card                             | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityCode__c                              | Insurance Code                           | CRUD                            | R            | R                      |
| vlocity_ins__VlocityContractServiceLog__c                | Vlocity Contract Service Log             | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityDataPack__c                          | Vlocity DataPack Object                  | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityDocuSignBranding__c                  | Vlocity DocuSign Branding                | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityDocuSignTemplate__c                  | Vlocity DocuSign Template                | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityErrorLogEntry__c                     | Vlocity Error Log Entry                  | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityFunction__c                          | Vlocity Function                         | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityFunctionArgument__c                  | Vlocity Function Argument                | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityScheduledJob__c                      | Vlocity Scheduled Job                    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocitySearchWidgetActionsSetup__c          | Vlocity Interaction Launcher Action      | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocitySearchWidgetSetup__c                 | Vlocity Interaction Launcher             | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityState__c                             | Vlocity State                            | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityStateModel__c                        | Vlocity State Model                      | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityStateModelVersion__c                 | Vlocity State Model Version              | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityStateTransition__c                   | Vlocity State Transition                 | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityStateTransitionRule__c               | Vlocity State Transition Rule            | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocitySystemLog__c                         | Vlocity System Log                       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityTrackingComponent__c                 | Vlocity Tracking Component               | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityTrackingEntry__c                     | Vlocity Tracking Entry                   | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityTrackingEvent__e                     | Vlocity Tracking Event                   | CR                              | CR           | CR                     |
| vlocity_ins__VlocityTrackingGroup__c                     | Vlocity Tracking Group                   | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityUILayout__c                          | Vlocity UI Layout                        | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityUITemplate__c                        | Vlocity UI Template                      | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityWebTrackingConfiguration__c          | Vlocity Web Tracking Configuration       | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VlocityWebTrackingEventType__c              | Vlocity Web Tracking Event Type          | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VqMachine__c                                | Vlocity Intelligence Machine             | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VqMachineResource__c                        | Vlocity Intelligence Machine Resource    | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins__VqResource__c                               | Vlocity Intelligence Resource            | CRUV                            | CRUV         | CRUV                   |
| vlocity_ins_fsc__CommissionStatement__c                  | Commission Statement                     | CRUD                            |              |                        |
| vlocity_ins_fsc__InsPaymentScheduleEntryDetail__c        | Insurance Payment Schedule Entry Detail  | CRUD                            | R            | R                      |
| vlocity_ins_fsc__InsurancePolicyPaymentScheduleEntry__c  | Insurance Policy Payment Schedule Entry  | R                               | R            | R                      |
| vlocity_ins_fsc__InsurancePolicyTerm__c                  | Insurance Policy Terms                   | R                               | R            | R                      |
| vlocity_ins_fsc__InsurancePolicyTermTrackingEntry__c     | Insurance Policy Terms Tracking Entry    | CRUD                            | R            | R                      |
| WorkerCompCoverageClass                                  | Worker Compensation Coverage Class       | CRUV                            | CRUV         | CRUV                   |
| WorkOrder                                                | Work Order                               | CRUV                            | CRUV         | CRUV                   |

12.2	Permisos del Perfil x Apps: 

* A continuación se encuentra la relación de permisos a nivel de Apps por cada Perfil.

<!-- 13 -----------------------------------------------------Permission set Group----------------------------------------------------------------------- -->

## 13. Permission set Group

13.1 Definición de Permission set Group por perfil:
	
| Perfil                 | Permission Set Group    |
| ---------------------- | ----------------------- |
| Profesional Comercial  | PSGProfesionalComercial |
| Jefe Tecnico           | PSGJefeTecnico          |
| Tecnico de operaciones | PSGTecnicoDeOperaciones |

Descripción de cada Permission set Group y las respectivas licencias que se utilizan:

* PSGProfesionalComercial
  
	| Permission Set Label                                        | License                                      |
	| ----------------------------------------------------------- | -------------------------------------------- |
	| ActionPlans                                                 | Action Plans                                 |
	| Analytics Integration                                       |                                              |
	| Aura-Enabled Apex Class Access for Financial Services Cloud |                                              |
	| CLMInd Runtime All                                          |                                              |
	| CRM User                                                    | CRM User                                     |
	| DocGenInd HINS Designer User                                | Document Generation User for HINS Industries |
	| DocGenInd HINS Runtime User                                 | Document Generation User for HINS Industries |
	| Document Checklist                                          | Document Checklist                           |
	| FSC Insurance                                               | FSC Insurance                                |
	| Financial Services Cloud Standard                           | Financial Services Cloud Standard            |
	| Insurance Commissions for Create/Update Quote               |                                              |
	| Insurance Create/Update Census Data                         |                                              |
	| Insurance Create/Update Group Census Data                   |                                              |
	| Insurance Create/Update Group Census Quote                  |                                              |
	| Insurance Create/Update Policy                              |                                              |
	| Insurance Group Benefits Package                            | Insurance Group Benefits Package             |
	| Insurance Policy and Claims                                 | Insurance Policy and Claims                  |
	| Insurance Product Catalog Admin Package                     | Insurance Product Administration Package     |
	| Insurance Quoting Package                                   |                                              |
	| Insurance Self Quoting                                      |                                              |
	| Insurance View Group Census Data                            |                                              |
	| Insurance View Group Census Quote                           |                                              |
	| OmniStudio Admin                                            | OmniStudio                                   |
	| Rule Engine Runtime                                         | Business Rules Engine Runtime                |

* PSGJefeTecnico

	| Permission Set Label                                        | License                                      |
	| ----------------------------------------------------------- | -------------------------------------------- |
	| ActionPlans                                                 | Action Plans                                 |
	| Analytics Integration                                       |                                              |
	| Aura-Enabled Apex Class Access for Financial Services Cloud |                                              |
	| CLMInd Runtime All                                          |                                              |
	| CRM User                                                    | CRM User                                     |
	| DocGenInd HINS Designer User                                | Document Generation User for HINS Industries |
	| DocGenInd HINS Runtime User                                 | Document Generation User for HINS Industries |
	| Document Checklist                                          | Document Checklist                           |
	| FSC Insurance                                               | FSC Insurance                                |
	| Financial Services Cloud Standard                           | Financial Services Cloud Standard            |
	| Insurance Commissions for Create/Update Quote               |                                              |
	| Insurance Create/Update Census Data                         |                                              |
	| Insurance Create/Update Group Census Data                   |                                              |
	| Insurance Create/Update Group Census Quote                  |                                              |
	| Insurance Create/Update Policy                              |                                              |
	| Insurance Group Benefits Package                            | Insurance Group Benefits Package             |
	| Insurance Policy and Claims                                 | Insurance Policy and Claims                  |
	| Insurance Product Catalog Admin Package                     | Insurance Product Administration Package     |
	| Insurance Quoting Package                                   |                                              |
	| Insurance Self Quoting                                      |                                              |
	| Insurance View Group Census Data                            |                                              |
	| Insurance View Group Census Quote                           |                                              |
	| OmniStudio Admin                                            | OmniStudio                                   |
	| Rule Engine Runtime                                         | Business Rules Engine Runtime                |

* PSGTecnicoDeOperaciones
  
	| Permission Set Label                                        | License                                      |
	| ----------------------------------------------------------- | -------------------------------------------- |
	| ActionPlans                                                 | Action Plans                                 |
	| Analytics Integration                                       |                                              |
	| Aura-Enabled Apex Class Access for Financial Services Cloud |                                              |
	| CLMInd Runtime All                                          |                                              |
	| CRM User                                                    | CRM User                                     |
	| DocGenInd HINS Designer User                                | Document Generation User for HINS Industries |
	| DocGenInd HINS Runtime User                                 | Document Generation User for HINS Industries |
	| Document Checklist                                          | Document Checklist                           |
	| FSC Insurance                                               | FSC Insurance                                |
	| Financial Services Cloud Standard                           | Financial Services Cloud Standard            |
	| Insurance Commissions for Create/Update Quote               |                                              |
	| Insurance Create/Update Census Data                         |                                              |
	| Insurance Create/Update Group Census Data                   |                                              |
	| Insurance Create/Update Group Census Quote                  |                                              |
	| Insurance Create/Update Policy                              |                                              |
	| Insurance Group Benefits Package                            | Insurance Group Benefits Package             |
	| Insurance Policy and Claims                                 | Insurance Policy and Claims                  |
	| Insurance Product Catalog Admin Package                     | Insurance Product Administration Package     |
	| Insurance Quoting Package                                   |                                              |
	| Insurance Self Quoting                                      |                                              |
	| Insurance View Group Census Data                            |                                              |
	| Insurance View Group Census Quote                           |                                              |
	| OmniStudio Admin                                            | OmniStudio                                   |
	| Rule Engine Runtime                                         | Business Rules Engine Runtime                |

13.2 Asignar Permission set Group x Usuario:

Se debe asignar el Permission set Group al usuario creado.
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/PermissionSetGroupAssigned.png?raw=true" width=500>
	</p>  	

<!-- 14 -----------------------------------------------------libreria de templates----------------------------------------------------------------------- -->

## 14. Acceso Libreria Vlocity Document Template


* Cambiar a salesforce classic

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateVerClassic.png?raw=true" width=500>
	</p>  

 * Acceda a todos los Tabs

 	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateMas.png?raw=true" width=500>
	</p> 

 * Acceda a la opción de librerias

	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateLibrerias.png?raw=true" width=500>
	</p> 

 * Seleccione la libreria Vlocity Document Template
   
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateSelectTemplate.png?raw=true" width=500>
	</p> 
   
 * Agregue los usuarios que necesitan crear o consultar templates

   	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateAddMember.png?raw=true" width=500>
	</p> 

 * Busque y seleccione el usuario a asignar
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/assets/9698159/e42d3228-9e03-4378-91d0-e76b64b16060" width=500>
	</p> 
 * Confirme la selección del usuario
   	 <p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateAddMember3.png?raw=true" width=500>
	</p> 
* Otorge permisos de administración a la libreria
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateAddMember4.png?raw=true" width=500>
	</p>
* Verifique la asignación del usuario
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/AccesoLibreriasTemplateAddMember5.png?raw=true" width=500>
	</p> 

 <!-- 15 -----------------------------------------------------Approval Processes----------------------------------------------------------------------- -->

## 15. Approval Processes

Para acceder a este modulo: 

* Setup
* Process Automation
* Approval Processes
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcesses.png?raw=true" width=500>
	</p> 

15.1 Para usuarios cuyo perfil es el de Tecnico Operaciones:

* En el filtro de Approval Processes seleccione : Document Checklist Item
* Acceda al Approval Processes : DocumentApproval  
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesDocumentCheckList.png?raw=true" width=500>
	</p> 
* En la sección Approval Steps, edite el paso : Approval
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps.png?raw=true" width=500>
	</p> 
* Clic en Next
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps1.png?raw=true" width=500>
	</p> 

* Clic en Next
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps2.png?raw=true" width=500>
	</p> 

* Clic en Add Row para agregar un nuevo usuario
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps3.png?raw=true" width=500>
	</p> 
 
* Clic en el buscador
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps4.png?raw=true" width=500>
	</p> 
 
* Seleccione el Usuario
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps5.png?raw=true" width=500>
	</p> 
* Guarde los cambios realizados
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps6.png?raw=true" width=500>
	</p> 
* Verifique la asignación del usuario
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps7.png?raw=true" width=500>
	</p> 
15.2 Para usuarios cuyo perfil es el de Jefe Tecnico:

* En el filtro de Approval Processes seleccione : Quote
* Acceda a los dos Approval Processes diseñados : Aprobacion Plan Abierto y Approval Commission
	<p>
	  <img src = "https://github.com/cloudblueadmin/global-core/blob/main/ApprovalProcessesSteps8.png?raw=true" width=500>
	</p> 

Realice los pasos descritos en el punto 15.1 con los usuarios de interes que desea asignar a dichos Approval Processes.
