# calendar-handphone
手机端日历 基于angularu1开发引入咯touch模块
456465
index.html code:
```
<!DOCTYPE html>
<html ng-app='myApp' lang="zh-cn">
<head>
    <title>Untitled Document</title>
    <meta charset="UTF-8">
    <meta name="description" content="" />
    <meta name="keywords" content="" />
    <meta name="viewport" content="width=device-width" />
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        table{
            border-collapse: collapse;
            font-size: 10px;
        }
        table td,table th{
            border: 1px solid #eee;
            text-align: center;
/*            padding: 20px;*/
/*            height: 40px;*/
        }
        table th{
            width:14.28%;
            padding: 20px 0;
        }
        table td{
            
            
        }
        td a{
            display: block;
            position: relative;
            padding: 20px 0;
            color: #696969;
            text-decoration: none;
        }
        td a:hover{
/*            background-color: #e0366e;*/
/*            color: #fff;*/
        }
        td a .tips{
            position: absolute;
            right: 5px;
            line-height: 18px;
            font-size: 10px;
            top: 5px;
            display: block;
            border-radius: 50px;
            width: 18px;
            text-align: center;
            height: 18px;
            background-color: #09D806;
            color: #fff;
        }
    </style>
</head>
<body ng-controller='calendar'>
<div class="calendar" ng-swipe-left="aa()" ng-swipe-right="bb()" ng-swipe-right="calendarss.nextMonth()"></div>
</body>
    <script src="js/jquery.min.js"></script>
    <script src="js/test.js"></script>
    <script src="js/angular.min.js"></script>
    <script src="js/angular-touch.min.js"></script>
    <script>
        var app = angular.module('myApp',['ngTouch']);
        function calendarController($scope){
            var calendarss = new calendars();
            calendarss.calendar();
            $scope.bb = function(){
                calendarss.prevMonth();
            };
            $scope.aa = function(){
                calendarss.nextMonth();
            };
            $scope.$on('name',function(){
                console.log('name');
            });
        }
        app.controller('calendar',['$scope',calendarController]);
    </script>
</html>
```
