# 🤖 agent.md — Next.js Auth Project (Signin & Signup)

## 📌 Project Overview

| Field | Details |
|---|---|
| **Project Name** | next-auth-learning |
| **Goal** | Signin & Signup authentication শেখা |
| **Stack** | Next.js (latest) + TypeScript + Zod + React Hook Form + MongoDB + NextAuth |
| **Learner Level** | Beginner → Intermediate |
| **Language** | বাংলায় explain, English-এ code |

---

## 🧠 AI-কে কীভাবে ব্যবহার করবে (Core Rules)

### ❌ কখনো বলো না
```
"এই feature বানিয়ে দাও"
"পুরো page-টা লিখে দাও"
"Fix করে দাও"
```

### ✅ সবসময় বলো
```
"Concept বোঝাও, আমি নিজে লিখবো"
"ছোট ছোট step-এ guide করো"
"Hint দাও, সরাসরি answer না"
```

---

## 🎯 Branch Prompt Templates

### যেকোনো Branch শুরু করার আগে এই template ব্যবহার করো:

```
আমি Next.js (latest) + TypeScript দিয়ে authentication project শিখছি।
আজকে আমি [BRANCH NAME] করতে চাই।

আমি beginner, তাই:
1. আগে concept বোঝাও (বাংলায়)
2. তারপর ছোট ছোট step-এ code-এর structure দাও
3. প্রতিটা line কী করছে সেটা explain করো
4. আমি লিখে নিলে পরের step দাও

বাংলায় explain করো।
```

---

## 🌿 Branch Structure

### Branch 1 — `feature/ui-setup`
**লক্ষ্য:** Project setup + Signin/Signup UI তৈরি করা

**শেখার Topics:**
- Next.js (latest) App Router structure
- TypeScript basics (types, interfaces)
- Tailwind CSS + shadcn/ui components
- Folder structure best practices

**AI Prompt:**
```
আমি Next.js (latest) App Router দিয়ে signin আর signup page বানাতে চাই।
TypeScript আর Tailwind ব্যবহার করবো।
আগে বোঝাও:
- App Router-এ page কোথায় বানাবো?
- TypeScript-এ component কীভাবে লিখি?
তারপর step-by-step guide করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
app/
  (auth)/
    signin/
      page.tsx
    signup/
      page.tsx
components/
  ui/
    AuthForm.tsx
```

---

### Branch 2 — `feature/zod-validation`
**লক্ষ্য:** Form data validate করতে Zod শেখা

**শেখার Topics:**
- Zod schema কী এবং কেন দরকার
- Type inference with Zod
- Custom error messages বাংলায়/ইংরেজিতে
- Password strength validation

**AI Prompt:**
```
আমি Zod দিয়ে signup form validate করতে চাই।
Fields: name, email, password, confirmPassword

আগে বোঝাও:
- Zod schema মানে কী? Real life example দিয়ে বোঝাও।
- z.object() কীভাবে কাজ করে?
তারপর step-by-step schema বানাতে help করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
lib/
  validations/
    auth.schema.ts
```

---

### Branch 3 — `feature/react-hook-form`
**লক্ষ্য:** Form handling + Zod এর সাথে connect করা

**শেখার Topics:**
- useForm hook কীভাবে কাজ করে
- zodResolver দিয়ে Zod connect করা
- Error messages display করা
- Form submission handling

**AI Prompt:**
```
আমি React Hook Form আর Zod একসাথে ব্যবহার করতে চাই।
signup form-এ validation add করবো।

আগে বোঝাও:
- useForm hook কী করে? Controlled vs Uncontrolled form কী?
- zodResolver কীভাবে কাজ করে?
তারপর আমার AuthForm.tsx-এ কীভাবে add করবো সেটা step-এ বোঝাও।
বাংলায় বোঝাও।
```

---

### Branch 4 — `feature/mongodb-setup`
**লক্ষ্য:** MongoDB connect করা + User model বানানো

**শেখার Topics:**
- MongoDB Atlas setup
- Mongoose connection in Next.js
- User Schema + Model তৈরি
- Environment variables (.env.local)

**AI Prompt:**
```
আমি Next.js (latest)-এ MongoDB Mongoose দিয়ে user data save করতে চাই।

আগে বোঝাও:
- Next.js-এ MongoDB connect করার সবচেয়ে ভালো pattern কী?
- Mongoose Schema আর Model-এর পার্থক্য কী?
তারপর step-by-step:
1. connection utility file
2. User model
বানাতে help করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
lib/
  db/
    mongoose.ts
models/
  User.ts
```

---

### Branch 5 — `feature/nextauth-setup`
**লক্ষ্য:** NextAuth.js দিয়ে actual authentication

**শেখার Topics:**
- NextAuth Credentials Provider
- JWT vs Session কী পার্থক্য
- Password hashing with bcryptjs
- Protected routes middleware

**AI Prompt:**
```
আমি NextAuth.js দিয়ে credentials-based authentication করতে চাই।
User email + password দিয়ে login করবে।

আগে বোঝাও:
- NextAuth কীভাবে কাজ করে? Session কোথায় থাকে?
- Credentials Provider মানে কী?
- Password কেন hash করতে হয়?
তারপর step-by-step:
1. NextAuth config
2. API route
3. Signup API
বানাতে help করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
app/
  api/
    auth/
      [...nextauth]/
        route.ts
      signup/
        route.ts
lib/
  auth/
    options.ts
```

---

### Branch 6 — `feature/tanstack-query`
**লক্ষ্য:** API calls manage করতে TanStack Query শেখা

**শেখার Topics:**
- useMutation কী এবং কেন
- Loading/Error state handle করা
- Query invalidation
- Optimistic updates

**AI Prompt:**
```
আমি TanStack Query দিয়ে signup আর signin API call করতে চাই।

আগে বোঝাও:
- TanStack Query কেন দরকার? Fetch directly করলে কী সমস্যা?
- useMutation কীভাবে কাজ করে?
তারপর signup form-এ useMutation add করতে step-by-step help করো।
বাংলায় বোঝাও।
```

---

### Branch 7 — `feature/email-verification`
**লক্ষ্য:** Signup-এর পরে email verification করা

**শেখার Topics:**
- Nodemailer দিয়ে email পাঠানো
- Verification token generate করা (crypto)
- Token expire time set করা
- Email template বানানো (HTML email)
- Verified/Unverified user flow

**AI Prompt:**
```
আমি email verification feature বানাতে চাই।
User signup করলে email যাবে, link click করলে verified হবে।

আগে বোঝাও:
- Email verification কীভাবে কাজ করে? Real life example দিয়ে বোঝাও।
- Verification token কী? কেন expire time দরকার?
- Nodemailer কীভাবে setup করতে হয়?
তারপর step-by-step:
1. Token generate করা
2. Email পাঠানো
3. Verify API route
বানাতে help করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
lib/
  email/
    mailer.ts
    templates/
      verification.ts
app/
  api/
    auth/
      verify-email/
        route.ts
      resend-verification/
        route.ts
models/
  VerificationToken.ts
```

---

### Branch 8 — `feature/forgot-password`
**লক্ষ্য:** Password reset flow implement করা

**শেখার Topics:**
- Password reset token generate করা
- Reset link email-এ পাঠানো
- Token validate করা (expire check)
- নতুন password save করা (hash করে)
- Security best practices

**AI Prompt:**
```
আমি forgot password feature বানাতে চাই।
User email দেবে, reset link যাবে, link দিয়ে নতুন password দেবে।

আগে বোঝাও:
- Password reset flow কীভাবে কাজ করে?
- Reset token কেন one-time use হওয়া দরকার?
- Token expire কেন গুরুত্বপূর্ণ?
তারপর step-by-step:
1. Forgot password form + API
2. Reset token email
3. New password form + API
বানাতে help করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
app/
  (auth)/
    forgot-password/
      page.tsx
    reset-password/
      page.tsx
  api/
    auth/
      forgot-password/
        route.ts
      reset-password/
        route.ts
models/
  PasswordResetToken.ts
```

---

### Branch 9 — `feature/role-based-auth`
**লক্ষ্য:** Admin আর User-এর জন্য আলাদা access control

**শেখার Topics:**
- User model-এ role field (admin/user) যোগ করা
- NextAuth session-এ role include করা
- Role-based middleware দিয়ে route protect করা
- Admin dashboard বানানো
- useSession দিয়ে client-side role check

**AI Prompt:**
```
আমি role-based authentication করতে চাই।
Admin আলাদা dashboard দেখবে, User আলাদা।

আগে বোঝাও:
- RBAC (Role-Based Access Control) কী?
- NextAuth session-এ custom data কীভাবে রাখি?
- Middleware দিয়ে route protect কীভাবে করি?
তারপর step-by-step:
1. User model-এ role যোগ করা
2. Session-এ role include করা
3. Admin route protect করা
বানাতে help করো।
বাংলায় বোঝাও।
```

**Files যা বানাবে:**
```
app/
  (protected)/
    admin/
      page.tsx
      dashboard/
        page.tsx
    user/
      profile/
        page.tsx
middleware.ts
lib/
  auth/
    roles.ts
types/
  next-auth.d.ts
```

---

### Branch 10 — `feature/deploy-vercel`
**লক্ষ্য:** Production-এ deploy করা এবং environment configure করা

**শেখার Topics:**
- Vercel-এ Next.js deploy করার process
- Environment variables Vercel-এ set করা
- MongoDB Atlas production connection string
- NextAuth production URL configure করা
- Domain + SSL setup
- Build error debug করা

**AI Prompt:**
```
আমি আমার Next.js auth project Vercel-এ deploy করতে চাই।

আগে বোঝাও:
- Development আর Production environment-এর পার্থক্য কী?
- কোন environment variables production-এ দরকার?
- MongoDB Atlas production-এর জন্য কীভাবে configure করতে হয়?
তারপর step-by-step deploy করতে help করো।
বাংলায় বোঝাও।
```

**Production Checklist:**
```
NEXTAUTH_URL=https://your-domain.vercel.app
NEXTAUTH_SECRET=[strong random secret]
MONGODB_URI=[MongoDB Atlas production URI]
EMAIL_HOST=[SMTP host]
EMAIL_USER=[email address]
EMAIL_PASS=[app password]
```

**Files যা বানাবে/check করবে:**
```
.env.example          ← সব variable-এর template (value ছাড়া)
next.config.ts        ← production config check
vercel.json           ← optional Vercel config
```

---

## 🔴 Error Handling Protocol

Error হলে **কখনো সরাসরি fix চেয়ো না।** এই template ব্যবহার করো:

```
আমি এই code লিখেছি:
[তোমার code paste করো]

এই error আসছে:
[error message paste করো]

আমি নিজে বুঝতে চাই।
- কোন line-এ সমস্যা হতে পারে সেটা hint দাও
- কেন এই error আসছে সেটা বোঝাও
- সরাসরি fix দিও না
বাংলায় বোঝাও।
```

---

## ❓ Concept বোঝার প্রশ্নগুলো

যেকোনো কিছু না বুঝলে এই তিনটা প্রশ্ন করো:

```
1. "এই line-টা কেন লিখলাম, এটা না লিখলে কী হতো?"
2. "এই concept-টা একটা real life example দিয়ে বোঝাও"
3. "আমি এইভাবে লিখেছি — এটা কি ঠিক আছে, নাকি better way আছে?"
```

---

## 📋 Git Workflow

```bash
# প্রতিটা Branch-এর শুরুতে
git checkout main
git pull origin main
git checkout -b feature/branch-name

# কাজ শেষে
git add .
git commit -m "feat: [কী করলে সেটা লেখো]"
git push origin feature/branch-name
```

**Commit message examples:**
```
feat: add signup page UI with shadcn components
feat: add zod validation schema for auth forms
fix: fix email validation error message
```

---

## 🛠️ Tech Stack & Versions

```json
{
  "framework": "Next.js (latest) (App Router)",
  "language": "TypeScript",
  "styling": "Tailwind CSS + shadcn/ui",
  "validation": "Zod",
  "forms": "React Hook Form",
  "database": "MongoDB + Mongoose",
  "auth": "NextAuth.js v5",
  "data-fetching": "TanStack Query v5",
  "email": "Nodemailer",
  "deployment": "Vercel",
  "package-manager": "yarn"
}
```

---

## 🚀 Project Setup Command

```bash
# Project তৈরি করো
npx create-next-app@latest next-auth-learning --typescript --tailwind --app

cd next-auth-learning

# Dependencies install করো
yarn add zod react-hook-form @hookform/resolvers
yarn add mongoose
yarn add next-auth@beta
yarn add @tanstack/react-query
yarn add bcryptjs nodemailer
yarn add -D @types/bcryptjs @types/nodemailer

# shadcn/ui init
npx shadcn-ui@latest init
```

---

## ✅ Learning Checklist

- [ ] Branch 1: Project setup + UI বানিয়েছি
- [ ] Branch 2: Zod schema বুঝেছি এবং লিখেছি
- [ ] Branch 3: React Hook Form + Zod connect করেছি
- [ ] Branch 4: MongoDB connect + User model বানিয়েছি
- [ ] Branch 5: NextAuth দিয়ে login/signup কাজ করছে
- [ ] Branch 6: TanStack Query দিয়ে API call করছি
- [ ] Branch 7: Email verification কাজ করছে
- [ ] Branch 8: Forgot/Reset password flow কাজ করছে
- [ ] Branch 9: Admin/User role-based access কাজ করছে
- [ ] Branch 10: Vercel-এ successfully deploy করেছি 🚀

---

> 💡 **মনে রাখো:** Video দেখো concept বোঝার জন্য। Code করো AI-এর সাথে।
> এই দুটো মিলিয়ে শিখলেই সবচেয়ে দ্রুত শিখবে। 🚀