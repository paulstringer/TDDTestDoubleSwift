#An example project for exploring use of Test Doubles and Mocks to facilitate TDD in Swift.

This example is based on excercises originally described in Michael Feathers, Working Effectively with Legacy Code, Chapter 3, Sensing and Collaboration.

1. Link Pod 'Cuckoo' to test target
2. Add the [Run Script](http://cocoadocs.org/docsets/Cuckoo/0.4.0/) to test target
3. Add Display.swift and add to files to Mock
4. Add the GeneratedMocks.swift to Test Target
5. Write a failing test
	1. Create a Mock Display Object e.g. ```MockDisplay()```
	2. Inject Mock Display e.g. ```Sale(display: mockDisplay)```
	3. Stub showLine e.g. ```when(mock.showLine(anyString())).thenReturn()```
	3. Verify Mock Display e.g. ```verify(mockDisplay).showLine("")```
6. Pass the Test

As a further excercise repeat the above again but instead use classic TDD and a simple 'Spy' Test Double object.