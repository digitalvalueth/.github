# Digital Value Project Naming Standards

เอกสารฉบับนี้กำหนดมาตรฐานการตั้งชื่อ (Naming Convention) สำหรับ Repository และ Git Workflow เพื่อให้การทำงานร่วมกันในทีม **Digital Value** เป็นไปอย่างมีระบบและเป็นสากล

---

## 1. Repository Naming (การตั้งชื่อโปรเจกต์)

เราจะใช้รูปแบบ **kebab-case** (ตัวพิมพ์เล็กทั้งหมด คั่นด้วยเครื่องหมาย `-`) ซึ่งเป็นมาตรฐานที่อ่านง่ายที่สุดบน URL

### โครงสร้างการตั้งชื่อ:
`[prefix]-[project-name]-[component/platform]`

### ส่วนประกอบ:
1.  **Prefix (Optional):** ระบุประเภทของงานเพื่อให้จัดกลุ่มได้ง่าย
    - `lib-` : สำหรับ Library หรือ Shared Code
    - `infra-` : สำหรับงาน Infrastructure / DevOps / Docker
    - `poc-` : สำหรับโปรเจกต์ทดลองหรือ Proof of Concept
    - `docs-` : สำหรับโปรเจกต์ที่เก็บเอกสารอย่างเดียว
2.  **Project Name:** ชื่อโปรเจกต์หลัก (ควรเป็นชื่อเฉพาะ)
3.  **Component/Platform:** ระบุส่วนงาน
    - `-api` : ส่วน Backend API
    - `-web` : ส่วน Frontend Web
    - `-mobile` : ส่วน Mobile Application
    - `-ui` : ส่วน UI Component หรือ Design System

### ตัวอย่างที่ถูกต้อง:
- `dv-accounting-api`
- `dv-hr-portal-web`
- `lib-thai-address-parser`
- `infra-k8s-production`

---

## 2. Branch Naming (การตั้งชื่อ Branch)

ในการพัฒนา เราจะแบ่งประเภท Branch ด้วย Prefix ตามลักษณะของงานที่ทำ ดังนี้:

| ประเภท | Prefix | ตัวอย่างการตั้งชื่อ |
| :--- | :--- | :--- |
| **ฟีเจอร์ใหม่** | `feature/` | `feature/user-authentication` |
| **แก้ไขบั๊ก** | `bugfix/` | `bugfix/login-error-on-ios` |
| **งานเร่งด่วน (Prod)** | `hotfix/` | `hotfix/security-patch-v1.1` |
| **เอกสาร** | `docs/` | `docs/update-api-spec` |
| **ปรับโครงสร้างโค้ด** | `refactor/` | `refactor/database-connection` |
| **เพิ่มประสิทธิภาพ** | `perf/` | `perf/optimize-image-loading` |

---

## 3. Commit Message Standards

เราแนะนำให้ใช้รูปแบบ **Conventional Commits** เพื่อให้ง่ายต่อการทำ Automated Changelog ในอนาคต

### รูปแบบ:
`<type>(scope): <description>`

### ตัวอย่าง:
- `feat(auth): add google oauth login`
- `fix(ui): fix sidebar overlap on mobile`
- `docs: update setup instructions in readme`
- `refactor(api): clean up unused controller methods`

---

## ข้อควรระวัง (Do Not)
- ❌ **ห้าม** ใช้ช่องว่าง (Space) ในการตั้งชื่อ
- ❌ **ห้าม** ใช้ตัวพิมพ์ใหญ่ (Uppercase) ในชื่อ Repository
- ❌ **ห้าม** ใช้ Under score (`_`) ให้ใช้ Dash (`-`) แทน
- ❌ **ห้าม** ตั้งชื่อที่ไม่มีความหมาย เช่น `project-v1`, `new-fix`, `test1234`

---

> **Note:** แก้ไขล่าสุด 25 December 2025 10:31:26 AM | Watthachai Taechalue
