All namespaces in this client library projects have a type that we call "model factory". 
Such types are called with the name of the namespace suffixed with "ModelFactory", e.g. OpenAI.Chat namespace has a factory type called OpenAIChatModelFactory.
These types are intended to provide a way to create instances of model types that otherwise coould not be instantiated and initialized using the model's constructors and properties, 
as some model types dont have necessary public constructors or property setters to do that. 
Often these constructors or setters are internal, as the model (usually a model used only as output) is instantiated by the library itself, not the user developer. 
In some scenarios (e.g. mocking for unit tests) the user wants to instantiate such output models, and so we provide model factories for these scenarios. 
Your task is to create a factory method for namespaces that miss those. 
