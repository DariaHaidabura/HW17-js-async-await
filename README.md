Создайте на вашем github репозиторий по следующему шаблону HW#-name. Все результаты нужно запушить в ваш репозиторий и прикрепить ссылку на hillel портале.
Создайте index.html в котором подключите js script.
Создайте README.md с описанием задания.
Напишите функцию timeout(data, ms), которая возвращает новый промис, переходящий в состояние "resolved" через ms миллисекунд и передает в резолв данные которые принимает через аргумент data. В реализации данной функции используем явные промисы.
Пример использования:
delay({name: "user"}, 1000).then((data) => console.log("Hello!", data))
Используйте async / await. Необходимо организовать цепочку промисов внутри асинхронной функции getResult.

	async function getResult() { тут должна быть цепочка вызовов }
Функции getUserInfo, getUserAvatar, getUserAdditionalInfo необходимо переписать в стиле async. Вместо setTimeout нужно использовать функцию delay которую написали в предыдущем задании (вызывать ее нужно через async await).		
​​Загрузить данные пользователя используем функцию getUserInfo.
Затем получить ссылку на аватар пользователя, для этого нужно использовать функцию getUserAvatar. Данная функция расширит и вернет обьект пользователя.
Затем получить дополнительную информацию по пользователю, для этого нужно использовать функцию getUserAdditionalInfo. Данная функция расширит и вернет обьект пользователя.
В конце вывести в консоль финальную версию полученного обьекта.
function getUserInfo() {
    return new Promise(function(resolve, reject) {
      setTimeout(() => resolve({ name: 'Vic', age: 21, id: 1 } ), 1000);
    });
  }
  function getUserAvatar(userInfo) {
    return new Promise(function(resolve, reject) {
