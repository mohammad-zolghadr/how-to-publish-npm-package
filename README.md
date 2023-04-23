## How To Publish React Npm Package in [npmjs.com](http://npmjs.com 'npmjs.com') with [Vite](http://vitejs.dev 'vitejs.dev')

## چجوری یه پکیج React.js رو توی سایت [npmjs.com](http://npmjs.com 'npmjs.com') با [Vite](http://vitejs.dev 'vitejs.dev') منتشر کنم؟

<img src="https://user-images.githubusercontent.com/48680310/233810433-824ec36e-33c2-4ee7-84fc-c121ebd055c0.png">

<h2 id="toc">Table Of Content</h2>
      <ul>
        <li>
          <details>
            <summary>
              <a href="#english-description">English Description</a>
            </summary>
            <ul>
              <li>
                <a href="#english-create-project">Create A Project With Vite</a>
              </li>
              <li>
                <details>
                  <summary>
                    <a href="#english-change-package-json"
                      >Change package.json</a
                    >
                  </summary>
                  <ul>
                    <li><a href="#english-desc">description</a></li>
                    <li><a href="#english-main">main</a></li>
                    <li><a href="#english-module">module</a></li>
                    <li><a href="#english-files">files</a></li>
                    <li><a href="#english-repo">repository</a></li>
                    <li><a href="#english-version">version</a></li>
                    <li><a href="#english-keyword">keywords</a></li>
                    <li><a href="#english-author">author</a></li>
                    <li><a href="#english-license">license</a></li>
                  </ul>
                </details>
              </li>
              <li>
                <a href="#english-structure-of-folder"
                  >Structure Of Package Folder</a
                >
              </li>
              <li><a href="#english-config-vite">Config Vite</a></li>
              <li><a href="#english-publish">Publish To Npm</a></li>
              <li><a href="#english-update">Update Package</a></li>
              <li><a href="#english-contact-me">Final word and Contact me</a></li>
            </ul>
          </details>
        </li>
        <li>
        <details>
            <summary>
              <a href="#persian-description">توضیحات فارسی</a>
            </summary>
            <ul>
              <li>
                <a href="#persian-create-project">ساختن پروژه جدید با Vite</a>
              </li>
              <li>
                <details>
                  <summary>
                    <a href="#persian-change-package-json"
                      >تغییر فایل package.json</a
                    >
                  </summary>
                  <ul>
                    <li><a href="#persian-desc">توضیحات</a></li>
                    <li><a href="#persian-main">فایل اصلی</a></li>
                    <li><a href="#persian-module">ماژول</a></li>
                    <li><a href="#persian-files">فایل ها</a></li>
                    <li><a href="#persian-repo">ریپازیتوری</a></li>
                    <li><a href="#persian-version">ورژن</a></li>
                    <li><a href="#persian-keywords">کلمات کلیدی</a></li>
                    <li><a href="#persian-author">توسعه دهنده</a></li>
                    <li><a href="#persian-license">لایسنس</a></li>
                  </ul>
                </details>
              </li>
              <li>
                <a href="#persian-structure-of-folder"
                  >ساختار پوشه پکیج</a
                >
              </li>
              <li><a href="#persian-config-vite">کانفیگ Vite</a></li>
              <li><a href="#persian-publish">انتشار پکیج</a></li>
              <li><a href="#persian-update">بروز رسانی پکیج</a></li>
              <li><a href="#persian-contact-me">سخن پایانی و ارتباط با من</a></li>
            </ul>
          </details>
          </li>
      </ul>

# <h1 id="english-description">English Description <a href="#toc">&uarr;</a> </h1>

## <h2 id="english-create-project">Create A Project With Vite <a href="#toc">&uarr;</a> </h2>

using npm :

`npm create vite`

using yarn :

`yarn create vite`

> Your project name will be the same as your project address on the npm site, so it must be a **unique name**. Before choosing a name for your project, **make sure that there is no such package with this name on the npm site**

## <h2 id="english-change-package-json">Change package.json <a href="#toc">&uarr;</a> </h2>

You need to add the following in the package.json file

### <h3 id="english-desc">description <a href="#toc">&uarr;</a> </h3>

A brief description of your project. You should add the full description in the README file

`"description" : "This package serves as the entry point to the DOM and server renderers for React"`

### <h3 id="english-main">main <a href="#toc">&uarr;</a> </h3>

Your final file that you need to publish (automatically created after the Build command)

> You can only change the name of the file, but make sure that the name you choose must be the same as the name you write in the **vite.config.js** file.

`"main" : "./dist/FINAL_PACKAGE_FILE_AFTER_BUILD.umd.js"`

### <h3 id="english-module">module <a href="#toc">&uarr;</a> </h3>

This file is automatically created like main and only you can change its name (not its format) and this name must be the same as you define in **vite.config.js** file.

`"module" : "./dist/FINAL_PACKAGE_FILE_AFTER_BUILD.es.js"`

### <h3 id="english-files">files <a href="#toc">&uarr;</a> </h3>

The files you want to publish on the npm site. Usually, the dist folder (created after build) and the README file are placed in this section

`"files" : ["dist" , "README.md"]`

### <h3 id="english-repo">repository <a href="#toc">&uarr;</a> </h3>

Enter the address of your git repository in this field

> Make sure that the word `git+` must be placed at the beginning of the url section, and after that, enter the repository address.

`"repository" : {"type" : "git" , "url" : "git+URL_OF_GIT_REPOSITORY"}`

### <h3 id="english-version">version <a href="#toc">&uarr;</a> </h3>

Your package version

> The first number from the left, for large and general changes,
> The middle number for moderate changes and simple new features
> And the number on the right is changed for very minor changes and simple bugs

`"version" : "1.0.0"`

### <h3 id="english-keywords">keywords <a href="#toc">&uarr;</a> </h3>

Keywords related to your package that can have a significant impact on SEO and finding your package. So fill this section carefully and patiently

`"keywords" : ["react" , "ui kit"]`

### <h3 id="english-author">author <a href="#toc">&uarr;</a> </h3>

The name of the group, organization or person who developed the package

`"author" : "Mohammad Zolghadr"`

### <h3 id="english-license">license <a href="#toc">&uarr;</a> </h3>

Enter your package license

`"license" : "MIT"`

---

## <h2 id="english-structure-of-folder">Structure Of Package Folder <a href="#toc">&uarr;</a> </h2>

- In the src folder, you created a new folder called lib
  `src>lib`
- In the lib folder, we have an **index.js** file that imports and exports all the parts of the package that we made.
  > All the files, functions, components, etc. that you want to publish must be entered in this file.

```javascript
import { yourPackageFunction } from './YOUR_FOLDER';
export { yourPackageFunction };
```

- In the lib folder, based on our project, we create folders related to the things we want to publish and note that import and export all of these in the primary index, i.e. `src>lib>index.js`

## <h2 id="english-config-vite">Config Vite <a href="#toc">&uarr;</a> </h2>

- install `path` package
  `npm i path` or `yarn add path`

- Change the** vite.config.js** file as follows

```javascript
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react-swc';
import path from 'path';

export default defineConfig({
  build: {
    lib: {
      entry: path.resolve(__dirname, 'src/lib/index.js'),
      name: 'NameOfYourPackage',
      fileName: (format) => `name.${format}.js`,
    },
    rollupOptions: {
      external: ['react', 'react-dom'],
      output: {
        globals: {
          react: 'React',
        },
      },
    },
  },
  plugins: [react()],
});
```

> 1. You only need to add the **build** section
> 2. The name you chose in the `fileName` section must be the same as the name you wrote in the `main` of package.json

## <h2 id="english-publish">Publish To Npm <a href="#toc">&uarr;</a> </h2>

- Create a free account at [npmjs.com](http://npmjs.com 'npmjs.com')
- Enter the **build** command in the terminal of your project
  `yarn build` or `npm run build`

  > With this, after a few seconds, your `dist` folder will be created, ready to publish to the npm site

- Enter the `npm login` command in the terminal and enter your account information
- We type the `npm publish` command in the terminal and after a few seconds, our package will be published on the npm website :)

## <h2 id="english-update">Update Package <a href="#toc">&uarr;</a> </h2>

If you want to release an **update** for your package, you should :

1. Change the package version in the **package.json** file
2. Run the **build** command to update the contents of the dist folder
3. Run the `npm publish` command to update the new version on the npm site

## <h2 id="english-contact-me">Final word and Contact me <a href="#toc">&uarr;</a> </h2>

I hope that you have made enough use of this document
If it works for you, I would appreciate it if you could encourage me by giving a star to this repo
If you want, you can connect with me in different social networks

gmail : [dev.mohammadzolghadr@gmail.com](https://mail.google.com/mail/?view=cm&fs=1&to=dev.mohammadzolghadr@gmail.com&su=Subject&body=Body) </br>
instagram : [mozo.plus](https://instagram.com/mozo.plus) </br>
linkedin : [mohammad-zolghadr](https://www.linkedin.com/in/mohammad-zolghadr/)</br>
myWebsite : [mohammadzolghadr.ir](https://mohammadzolghadr.ir)

# <h1 id="persian-description">توضیحات فارسی  <a href="#toc">&uarr;</a> </h1>

## <h2 id="persian-create-project">ساختن پروژه جدید با vite <a href="#toc">&uarr;</a> </h2>

استفاده از npm :

`npm create vite`

استفاده از yarn :

`yarn create vite`

> نام پروژه شما با آدرس url پروژه شما در سایت npm یکی خواهد بود، بنابراین باید یک **نام منحصر به فرد** انتخاب کنید. قبل از انتخاب نام برای پروژه، **مطمئن شوید که چنین پکیجی با این نام در سایت npm وجود ندارد**

## <h2 id="persian-change-package-json">تغییر فایل package.json <a href="#toc">&uarr;</a> </h2>

باید تغییرات زیر رو توی فایل package.json ایجاد کنی

### <h3 id="persian-desc">توضیحات <a href="#toc">&uarr;</a> </h3>

توضیحی کوتاه درمورد پکیج و نتیجه استفاده از پکیج رو اینجا بنویس. توضیحات کامل تر و نحوه استفاده از پکیج و.. رو بعدا توی فایل README باید اضافه کنی

`"description" : "This package serves as the entry point to the DOM and server renderers for React"`

### <h3 id="persian-main">فایل اصلی <a href="#toc">&uarr;</a> </h3>

آدرس فایل نهایی که قراره منتشر بشه (به صورت اتوماتیک توسط دستور Build ساخته میشه)

> شما فقط باید اسم فایل را تغییر بدی (نه فرمتش رو)، ولی حتما حواست باشه که اسمی رو که ایمنجا مینویسی باید دقیقا همون اسمی باشه که توی فایل **vite.config.js** می نویسی. (توی بخش کانفیگ Vite، درباره‌ش بیشتر توضیح میدیم)

`"main" : "./dist/FINAL_PACKAGE_FILE_AFTER_BUILD.umd.js"`

### <h3 id="persian-module">ماژول <a href="#toc">&uarr;</a> </h3>

این فایل هم اتوماتیک ساخته میشه (دقیقا مثل main) و فقط باید آدرس اسمش رو تغییر بدی (نه فرمتش رو) و این اسم هم باید دقیقا همون اسمی باشه که توی فایل **vite.config.js** تعریف کردی.

`"module" : "./dist/FINAL_PACKAGE_FILE_AFTER_BUILD.es.js"`

### <h3 id="persian-files">فایل ها <a href="#toc">&uarr;</a> </h3>

اینجا مشخص میکنی که کدوم فایل ها رو میخوای توی سایت npm منتشر کنی. معمولاً پوشه dist (که بعد از اجرای دستور Build به صورت اتوماتیک ساخته میشه) و فایل README رو توی این قسمت قرار میدیم

`"files" : ["dist" , "README.md"]`

### <h3 id="persian-repo">ریپازیتوری <a href="#toc">&uarr;</a> </h3>

آدرس ریپازیتوری گیت هاب رو توی این قسمت وارد کن

> دقت کن که کلمه `git+` باید توی قسمت اول url قرار بگیره و بعد از اون، آدرس گیت هاب رو وارد کن.

`"repository" : {"type" : "git" , "url" : "git+URL_OF_GIT_REPOSITORY"}`

### <h3 id="persian-version">ورژن <a href="#toc">&uarr;</a> </h3>

ورژن پکیجت توی این قسمت قرار میگیره

> اولین عدد از سمت چپ، برای تغییرات بزرگ و کلی،
> عدد وسط برای تغییرات متوسط ​​و ویژگی های جدید ساده
> و عدد سمت راست برای تغییرات بسیار جزئی و اشکالات و باگ های ساده تغییر می کنه

`"version" : "1.0.0"`

### <h3 id="persian-keywords">کلمات کلیدی <a href="#toc">&uarr;</a> </h3>

کلمات کلیدی که به نوعی به پکیجت مرتبط میشه رو اینجا بنویس. چون تاثیر بسزایی توی سئو و سرچ پکیجت داره، پس این قسمت رو با دقت و حوصله زیادی پر کن

`"keywords" : ["react" , "ui kit"]`

### <h3 id="persian-author">توسعه دهنده <a href="#toc">&uarr;</a> </h3>

اسم تیم، گروه، سازمان، یا هر شخصی که این پکیج رو توسعه داده رو توی این بخش وارد کن

`"author" : "Mohammad Zolghadr"`

### <h3 id="persian-license">لایسنس <a href="#toc">&uarr;</a> </h3>

لایسنس پکیجت رو اینجا وارد کن

`"license" : "MIT"`

---

## <h2 id="persian-structure-of-folder">ساختار پوشه پکیج <a href="#toc">&uarr;</a> </h2>

- توی پوشه src، یه پوشه جدید بساز به اسم lib. به این شکل
  `src>lib`
- توی پوشه lib، یه فایل **index.js** داریم (میسازیم) که همه توابع، کامپوننت ها و به طور کلی هر چیزی که ساختیم رو توی این فایل import و export میکنه.
  > همه فایل ها، توابع، کامپوننت ها و ... که میخوای منتشر کنی رو باید توی این فایل وارد بنویسی.

```javascript
import { yourPackageFunction } from './YOUR_FOLDER';
export { yourPackageFunction };
```

- توی پوشه lib، بر اساس پروژه‌مون، پوشه‌های مربوط به مواردی رو که میخوایم منتشر کنیم، ایجاد می‌کنیم و دقت کن که همه اینها رو توی فایل اولیه اصلی، یعنی `src>lib>index.js` باید import و export کنیم.

## <h2 id="persian-config-vite">کانفیگ کردن  Vite <a href="#toc">&uarr;</a> </h2>

- پکیج `path` رو با دستور `npm i path` یا `yarn add path` نصب کن

- فایل **vite.config.js** مثل زیر عوض کن

```javascript
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react-swc';
import path from 'path';

export default defineConfig({
  build: {
    lib: {
      entry: path.resolve(__dirname, 'src/lib/index.js'),
      name: 'NameOfYourPackage',
      fileName: (format) => `name.${format}.js`,
    },
    rollupOptions: {
      external: ['react', 'react-dom'],
      output: {
        globals: {
          react: 'React',
        },
      },
    },
  },
  plugins: [react()],
});
```

> 1. فقط بخش **build** رو باید اضافه کنی
> 2. اسمی رو که توی بخش `fileName` انتخاب میکنی، باید دقیقا همون اسمی باشه که برای بخش `main` توی فایل package.json نوشتی

## <h2 id="persian-publish">انتشار پکیج <a href="#toc">&uarr;</a> </h2>

- یه اکانت رایگان توی سایت [npmjs.com](http://npmjs.com 'npmjs.com') بساز
- دستور **build** رو توی ترمینال پروژه‌ت بنویس
  `yarn build` یا `npm run build`

  > با اینکار، پوشه `dist` در عرض چند ثانیه ساخته میشه و پکیجت آماده انتشاره

- دستور `npm login` رو توی ترمینال وارد کن و اطلاعات حسابت رو وارد کن که لاگین بشی
- دستور `npm publish` رو توی ترمینال بنویس و بعد از چند ثانیه میبینی که پکیجت با موفقیت توی سایت npm منتشر شده :)

## <h2 id="persian-update">بروز رسانی پکیج <a href="#toc">&uarr;</a> </h2>

اگه میخوای **نسخه جدید** از پکیجت رو منتشر کنی، باید :

1. ورژن پکیجت رو توی فایل **package.json** تغییر بدی
2. دستور **build** رو بزن که محتویات پوشه dist بر اساس آخرین تغییراتی که دادی، بروز بشن
3. دستور `npm publish` رو بزن تا ورژن جدید پکیجت، توی سایت npm، آپلود شه

## <h2 id="persian-contact-me">سخن نهایی و ارتباط با من <a href="#toc">&uarr;</a> </h2>

امیدوارم که از این داکیومنت، استفاده کافی رو برده باشی
اگه به دردت خورد، ممنون میشم که با ستاره دادن به این پروژه، باعث دلگرمی من بشی
اگه بخوای، میتونی باهام توی شبکه های اجتماعی مختلف در ارتباط باشی

gmail : [dev.mohammadzolghadr@gmail.com](https://mail.google.com/mail/?view=cm&fs=1&to=dev.mohammadzolghadr@gmail.com&su=Subject&body=Body) </br>
instagram : [mozo.plus](https://instagram.com/mozo.plus) </br>
linkedin : [mohammad-zolghadr](https://www.linkedin.com/in/mohammad-zolghadr/)</br>
myWebsite : [mohammadzolghadr.ir](https://mohammadzolghadr.ir)
