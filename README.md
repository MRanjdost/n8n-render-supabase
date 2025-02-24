مقدمه
n8n یک ابزار اتوماسیون قدرتمند است که می‌تواند برای ساخت ورک‌فلوهای پیچیده مورد استفاده قرار گیرد. در این راهنمایی، نحوه راه‌اندازی n8n روی Render.com و اتصال آن به دیتابیس Supabase را توضیح خواهیم داد.

تنظیمات مهم برای اجرای پروژه n8n
برای راه‌اندازی n8n در Render و اتصال آن به پایگاه داده Supabase، باید متغیرهای محیطی (Environment Variables) را به درستی پیکربندی کنید. این تنظیمات به شرح زیر هستند:

1. تنظیمات عمومی n8n
این تنظیمات برای تنظیم میزبان (host) و پورت n8n به‌کار می‌روند:

bash
Copy
Edit
N8N_HOST=<your_host>  # آدرس میزبان برای دسترسی به n8n
N8N_PORT=443  # پورت مورد استفاده برای اتصال https
N8N_PROTOCOL=https  # پروتکل ارتباطی
N8N_EDITOR_BASE_URL=<your_base_url>  # آدرس وب‌سایت n8n
WEBHOOK_URL=<your_webhook_url>  # URL مربوط به webhook برای دریافت داده‌ها
2. تنظیمات منطقه زمانی
برای اینکه زمان‌ها به‌درستی در n8n تنظیم شوند، باید منطقه زمانی را مشخص کنید:

bash
Copy
Edit
GENERIC_TIMEZONE=Europe/Berlin  # منطقه زمانی برای تمامی اتوماسیون‌ها
TZ=Europe/Berlin  # منطقه زمانی برای سیستم
3. تنظیمات رمزگذاری
این تنظیمات مربوط به رمزگذاری داده‌ها در n8n هستند:

bash
Copy
Edit
N8N_ENCRYPTION_KEY=<your_encryption_key>  # کلید رمزگذاری برای حفاظت از داده‌ها
4. تنظیمات پایگاه داده PostgreSQL (Supabase)
برای اتصال n8n به پایگاه داده PostgreSQL در Supabase، باید تنظیمات زیر را وارد کنید:

bash
Copy
Edit
DB_TYPE=postgresdb  # نوع پایگاه داده
DB_POSTGRESDB_SCHEMA=public  # اسکیمای پایگاه داده
DB_POSTGRESDB_HOST=<supabase_host>  # میزبان دیتابیس Supabase
DB_POSTGRESDB_DATABASE=postgres  # نام دیتابیس
DB_POSTGRESDB_PORT=<supabase_port>  # پورت پایگاه داده
DB_POSTGRESDB_USER=<supabase_user>  # نام کاربری برای اتصال به دیتابیس
DB_POSTGRESDB_PASSWORD=<supabase_password>  # رمز عبور برای اتصال به دیتابیس
مراحل راه‌اندازی پروژه
ثبت‌نام در Render.com: ابتدا در Render.com ثبت‌نام کنید و یک Web Service جدید بسازید.

ساخت n8n Web Service: پروژه n8n را در Render ایجاد کنید و تنظیمات فوق را برای راه‌اندازی آن به‌کار ببرید.

ساخت اکانت در Supabase: در Supabase ثبت‌نام کرده و یک پایگاه داده جدید ایجاد کنید.

اتصال n8n به Supabase: پس از ساخت پایگاه داده، اطلاعات اتصال به آن را در تنظیمات n8n وارد کنید.

نتیجه نهایی
پس از انجام تنظیمات، n8n به‌درستی با پایگاه داده Supabase شما متصل خواهد شد و می‌توانید از آن برای ایجاد اتوماسیون‌های پیچیده و انجام عملیات مختلف استفاده کنید.

پشتیبانی و منابع بیشتر
Render Documentation
Supabase Documentation
n8n Documentation
