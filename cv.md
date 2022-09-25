# Alexey Gavrikov

#### Junior Front-end Developer
___  

#### Contact information:

**Phone**: +7 910 496-23-37  
**Email**: a.e.gavrikoff@gmail.com  
**Telegram**: @methanoy  
**Discord**: Methanoy#5872  

___  

#### About Myself

In my work I have always been looking for an opportunity to expand the limits of knowledge, participate in interesting projects and feel the benefits of my work. At the same time I'm a lawyer, and my profession is associated with support someone who creating a product, while I would like to develop the products by myself.  
By 2019, I had already often encountered IT in my work (software delivery, SPA creation, cloud technologies) and came to the conclusion that I wanted to learn more about development and programming. Therefore, I began to study this area more, try different programming languages by SoloLearn / Coursera / Stepik / CodeAcademy, and by 2021 I finally decided to get a specialization of Frontend developer, so I signed up for Yandex.Practicum to study Web-development.  

___
#### Skills

- HTML5, CSS3  
- JavaScript, React.js  
- Node.js, Express.js  
- MongoDB  
- Webpack, npm, Git  

___  

#### Code example

User authentication function `login`. If the email and password match those in the database, the user logs in to the site. Otherwise - receives an error message. After authorization function `login` will make token and save it to cookie.

```javascript
const login = (req, res, next) => {
  const { email, password } = req.body;
  User
    .findUserByCredentials(email, password)
    .then((user) => {
      const token = jwt.sign(
        { _id: user._id },
        NODE_ENV === 'production' ? JWT_SECRET : 'some-secret',
        { expiresIn: '7d' },
      );

      res.cookie('jwt', token, {
        maxAge: 3600000 * 24 * 7,
        secure: NODE_ENV === 'production',
        httpOnly: true,
      })
        .send({ message: 'Вы успешно авторизовались.' });
    })
    .catch(next);
};
```
___  

#### Projects

**_Mesto_**  
- *Stack*: HTML, CSS (Flexbox / Grid / adaptive layout), JavaScript / React.js, Express.js, MongoDB, BEM, Git, Webpack.  
- *Functionality*: an interactive service with the ability to add / remove photo cards, edit a profile and like beautiful places from all over the world.  
- *Link to app*: <https://methanoy.nomoredomains.sbs>  
- *Frontend repo*: <https://github.com/Methanoy/react-mesto-auth>  
- *Backend repo*: <https://github.com/Methanoy/express-mesto-gha>  

**_Travel to Russia_**  
- *Stack*: HTML, CSS (Flexbox / Grid), BEM, Git.  
- *Functionality*: a one-page website with travel notes.  
- *Link to app*: <https://methanoy.github.io/russian-travel/>  
- *Repo*: <https://github.com/methanoy/russian-travel>  

**_Learn to learn_**  
- *Stack*: HTML, CSS (Flexbox), YouTube API, BEM, Git.  
- *Functionality*: a one-page website with usefull information about methods of increasing productivity in learning.  
- *Link to app*: <https://methanoy.github.io/how-to-learn/>  
- *Repo*: <https://github.com/methanoy/how-to-learn>  

___  

#### Courses

1. Yandex.Practicum - Web-developer (writing a diploma project).  
2. CodeAcademy - Frontend developer.  
3. Stepik - Security analysis of web-projects (in progress).  

___  

#### Languages

- Russian - native  
- English - intermediate  