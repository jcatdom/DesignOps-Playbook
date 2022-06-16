# S.O.L.I.D.

## Single Responsibility Principle (SRP)
An entity should only do one thing. Changes should not impact the overall system.

SRP can be applied to our entire codebase. Components can (and arguably should) do only one thing.

## Open-Closed Principle (OCP)
An entity should be open to extension, closed to manipulation.

OCP applies to all Components directly as data transfer is unidirectional (props are open, state is closed).

## Liskov substitution Principle (LSP)
Objects should be replaceable with objects of their subtype, without changing the correctness os usage.

LSP could work well as we are using TypeScript (JS would let us do anything we want without any type checks which makes it riskier.)

## Interface Segregation Principle (ISP)
Many specific interfaces are better than one large interface.

ISP again won't exactly be necessary for Components/Containers except deriving our props.

## Dependency Inversion Principle (DIP)
Depend on abstractions, not concretions.

React prefers composition over dependency injection so DIP isn’t applicable, although we can use it if it becomes beneficial. Existing means of dependency injection rely on injecting through a Component's props like MobX inject or through Redux connect which both inject a store as a prop.