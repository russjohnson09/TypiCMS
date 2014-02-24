# Mocking Public Static Methods


Static methods are not called on real objects, so normal mock objects can't mock
them. Mockery supports class aliased mocks, mocks representing a class name which
would normally be loaded (via autoloading or a require statement) in the system
under test. These aliases block that loading (unless via a require statement - so please
use autoloading!) and allow Mockery to intercept static method calls and add
expectations for them.