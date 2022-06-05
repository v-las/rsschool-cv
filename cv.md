# Vlas Mastykash

## QA Engeneer

---

### Contact Information

You can reach me at [Telegram][tg] | [WhatsApp][wa] | [e-mail][email] | [LinkedIn][in] | [Twitter][tw]

[email]: <mailto:mastykash.vlas@gmail.com>
[in]: <https://www.linkedin.com/in/v-las/>
[tg]: <https://t.me/v_las>
[wa]: <https://wa.me/79136198392>
[tw]: <https://twitter.com/v_las_>

### About myself

I've been a quality assurance engineer for a half of the year and I love my job!
My main goal is to help customers and developers find ways to improve products.
My priority is to investigate the product and find all kinds of defects.
I am a very caring team worker, keeping an eye on the product. And I am a fast learner.

### Skills and Proficiency

I'm using those tools at work: DevTools, Figma, Jira, DBeaver, Swagger, Postman.

<div align="center">
	<img alt="devtools" width="117px" src="https://user-images.githubusercontent.com/89486551/143319750-2f729405-4b8a-4f73-8e16-b5c7780517fc.png" />
	<img alt="figma" width="117px" src="https://user-images.githubusercontent.com/89486551/153722739-06821792-6882-4ca2-b6ba-8198944272be.png" />
	<img alt="jira" width="117px" src="https://user-images.githubusercontent.com/89486551/153722743-407bd6dd-f5bc-4b1a-8875-13969c69b517.png" />
	<img alt="dbeaver" width="117px" src="https://user-images.githubusercontent.com/89486551/143319757-0bbd31ce-7860-447a-9571-504653849d0b.png" />
	<img alt="PostgreSQL" width="117px" src="https://user-images.githubusercontent.com/89486551/143319773-17f2e07b-8dc2-4f02-9b60-e9f0b421ce06.png" />
	<img alt="swagger" width="117px" src="https://user-images.githubusercontent.com/89486551/153722742-ae154b3b-291e-4e94-a969-43dbcc537acd.png" />
	<img alt="postman" width="117px" src="https://user-images.githubusercontent.com/89486551/143319803-99550e9f-bdde-4354-b38a-a3aa8ffc9a77.png" />
</div>

And exploring those: GitBash (Terminal), Charles, JMeter, Fiddler, Android Studio, PyCharm, WebStorm.

<div align="center">
	<img alt="Git" width="102px" src="https://user-images.githubusercontent.com/89486551/143319775-c711ac23-04f8-44dd-9a0b-ea3698467e9e.png" />
	<img alt="Markdown" width="102px" src="https://user-images.githubusercontent.com/89486551/143319781-e0cb8223-f5db-4cfd-b2f8-9fab2e227023.png" />
	<img alt="charles" width="102px" src="https://user-images.githubusercontent.com/89486551/143319787-e5eb9aa4-5b57-454f-b903-64282274af76.png" />
	<img alt="jmeter" width="102px" src="https://user-images.githubusercontent.com/89486551/170130770-05666e29-abdc-43cb-9b85-b716c2509eae.png" />
	<img alt="fiddler" width="102px" src="https://user-images.githubusercontent.com/89486551/143319792-72034e75-f2fe-4589-b741-6f21a2433a71.png" />
	<img alt="android-studio" width="102px" src="https://user-images.githubusercontent.com/89486551/143319797-01713acf-1cc6-49c9-ae92-d520d55cef17.png" />
	<img alt="pycharm" width="102px" src="https://user-images.githubusercontent.com/89486551/143319814-3645ca4a-c3cc-4958-aa5b-ff27b47d704c.png" />
	<img alt="WebStorm" width="102px" src="https://user-images.githubusercontent.com/89486551/145703556-7853a2fb-9487-49c4-9ff9-868c0fb82a98.png" />
</div>

### Code Examples

**Get real-time exchange rates** task for Postman's sandbox from _Vadim Ksendzov's QA course_:
Get real-time exchange rates for all currencies from bank API, using one endpoint as an array with a list of currencies, and the second as a personal one for each currency rate.

```js
let jsonData = pm.response.json();
let currencyIds = [];

for (let count = 0; count < jsonData.length; count++) {
    currencyIds.push(jsonData[count].Cur_ID)
};

for (let count = 0; count < currencyIds.length; count++) {
    let currencyRequest = {
        url: pm.environment.get("baseUrl") + '/curr_byn',
        method: 'POST',
        header: {
            'Content-Type': 'multipart/form-data',
        },
        body: {
            mode: 'formdata',
            formdata: [
                {key: "auth_token", value: pm.environment.get("token")},
                {key: "curr_code", value: currencyIds[count]}
            ]
        },
    };

    pm.sendRequest(currencyRequest, (error, response) => {
        if (response.code != 200) {
            console.log('error');
        } else {
            let jsonData = response.json();
            console.log(jsonData.Cur_Name + " current rate is " + jsonData.Cur_OfficialRate);
        };
    });
};
```

### Experience

#### Purrweb

- **QA Engeneer** | Since Dec '21

### Education

- **Vadim Ksendzov's QA Engineer Course** | [ksendzov.com](https://ksendzov.com/)
- **Artsiom Rusau's QA Engineer Course** | [youtube.com](https://www.youtube.com/playlist?list=PLKbJd47Kcbju2Vhi-FL7AI14vItVmGYk-)
