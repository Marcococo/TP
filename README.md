# TP
TP5 du 11/0

<!doctype html>
<html ng-app>
<head>
<script type="text/javascript">
    function CodeController($scope){
        $scope.name=""
        $scope.code=['java','Css','html'];
        $scope.addCode=function(){
            $scope.code.push($scope.newCode);
        }
	$scope.deleteCode=function(index){
            $scope.code.splice(index,1);
        }
    }
</script>
</head>
<body>
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.1/angular.min.js"></script>
<div ng-controller="CodeController">

Identifiez vous et choisissez un code! <BR/>
    Enter Your Name : <input type="text" ng-model="name">
    Select a Code :
        <select ng-model="selectedCode" ng-options="code for code in code">
        </select>
    <hr/>
    List of Code :
    <ul>
		<li ng-repeat="code in code"> <a href ="https://www.google.fr/search?client=ubuntu&channel=fs&q={{code}}&ie=utf-8&oe=utf-8&gfe_rd=cr&ei=FebiVoPDFamx8wflnpnIDg"> {{code}} </a>  <button ng-click="deleteCode($index)"> Delete </button></li> 
    </ul>
    <hr />
    Name : {{name}}<br />
    Selected code : {{selectedCode}}
    <hr />
    More code :
        <input type="text" ng-model="newCode">
        <button ng-click="addCode()">Add</button>
	
</div>
</body>
</html>

rout provider 

ng view


