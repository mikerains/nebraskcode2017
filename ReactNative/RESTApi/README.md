# REST Api

HAL - Hypertext Application Language

The "rel" property describes the relationship of other URI's to this URI.
Fielding, HATEAOS

in Startup.cs, add JSON option
svc.addMvc().AddJsonOptions(()=>
{
options.SerializerSettings.ReferenceLoopHandling =
Newtonsoft.Json.ReferenceLoopHandling;
});

