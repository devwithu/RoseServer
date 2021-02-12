# RoseServer

원본
https://github.com/galaxywiz/RoseServer


서버프로그래밍 학습 및 코드 개선을 위해 레포지토리 복사함


윈도우10, 비주얼스튜디오 2019 에서 수정해야 할것
1. ServerCore/ServerLibrary/Util/ProgramValidation.h

 //this->checkSMTP();
 
 
2. ServerCore/ChattingServer/Server/UserManager.h

auto itr = userPool_.lower_bound(id); -> auto itr = userPool_.find(id);


3. ServerCore/ServerLibaray/Database/ADODatabase.cpp

db접속에 문제가 있을때 아래와 같이 시도해 볼수 있음.

글쓴 본인은 아래와 같이 외부DB서버로 시도해서 성공함.

snwprintf(buffer, L"Provider = sqloledb; Data Source = (도메인이름또는ip), 1433; Network Library = DBMSSOCN; Initial Catalog = TestDB; User ID = sa; Password = q1w2e3;");
    
