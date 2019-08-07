# moduleInterface
Python Simple Module Interface for framework

Installation :
    pip install moduleInterface

# Actuator
[ Module Interface Actuator Class ]

# Description
ModuleComponentInterface에 맞춘 규격의 

## Methods - Manage
1. init()
- Actuator 클래스의 초기화 작업을 수행합니다. 모듈 테이블과 객체 테이블이 모두 비워집니다.
2. clear()
- Actuator 클래스의 모든 테이블 내의 객체를 삭제하고 테이블을 비웁니다.

## Methods - Executor
1. open(object,id,value)
- 모듈 객체를 열 때 처리해야할 과정을 호출합니다.
2. close(object,id,value)
- 모듈 객체를 닫을 때 처리해야할 과정을 호출합니다.
3. get(object,attr)
- 모듈 객체에 해당하는 속성 정보를 얻습니다.
4. set(object,attr,value)
- 모듈 겍체에 해당하는 속성(attr) 정보를 value로 추가 및 변경합니다.
5. call(object,cmd,option)
- 모듈 객체를 명령 프로토콜(cmd)를 가지고 파라미터(option)을 부여하여 실행합니다. 모듈 실행 결과가 리턴됩니다.

## Methods - Loader
1. loadLibrary(module)
- module 이름을 가진 라이브러리를 모듈 테이블로 로드합니다. 인자 module은 string 타입입니다. 결과에 대한 bool 값이 리턴됩니다.
2. loadLibraryAs(module,alias)
- module 이름을 가진 라이브러리를 alias의 이름을 primary 키로 인식하여 모듈 테이블로 로드합니다. 결과에 대한 bool 값이 리턴됩니다. 인자 module과 alias는 은 string 타입입니다.
3. unloadLibrary(module)
- 모듈 테이블에 등록된 모듈을 언로드합니다. 인자 module은 string 타입입니다. 결과에 대한 bool 값이 리턴됩니다.
4. loadClass(module,class)
- 모듈 내 클래스를 객체를 생성하고, 객체가 성공적으로 생성되면 객체 테이블에 등록합니다. 인자 module과 class는 string 타입이고, class는 module 내부에 있는 class 이름입니다. 결과에 대한 bool 값이 리턴됩니다.
5. loadObject(name,class)
- class 객체를 name으로 객체 테이블에 등록합니다. 인자 module과 class는 string 타입입니다.
6. unloadObject(name)
- name으로 객체 테이블에 등록된 객체를 제거합니다.
7. getModuleHandle(module)
- 모듈 테이블에 module로 등록되었는지 확인합니다.
8. checkModuleLoaded(namespace)
- 모듈의 이름공간이 모듈 테이블에 로드 되어있는지 점검합니다. 결과에 대한 bool 값이 리턴됩니다.
9. getLoadedModuleList()
- 모듈 테이블을 사전 형식으로 복사합니다. 리턴된 객체를 수정해도 반영되지 않습니다. 
10. checkObjectLoaded(class)
- 객체 테이블에 class가 등록되었는지 확인합니다. 결과에 대한 bool 값이 리턴됩니다.
11. getLoadedObjectList()
- 객체 테이블을 사전 형식으로 복사합니다. 리턴된 객체를 수정해도 반영되지 않습니다. 
