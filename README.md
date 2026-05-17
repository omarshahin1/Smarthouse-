export default function SmartHouseERP() {
  const stats = {
    totalSales: '24,800 ج',
    todayProfit: '3,250 ج',
    cashBalance: '12,000 ج',
  };
  const cards = [
    { title: 'المبيعات', value: '12,450 ج', icon: '🛒' },
    { title: 'فودافون كاش', value: '7 عمليات', icon: '💳' },
    { title: 'الصيانة', value: '4 أجهزة', icon: '🛠️' },
    { title: 'التصوير 4×6', value: '38 صورة', icon: '📸' },
  ];

  const menu = [
    'لوحة التحكم',
    'المبيعات',
    'فودافون كاش',
    'الصيانة',
    'التصوير الفوتوغرافي',
    'الخدمات',
    'ماكينات فوري',
    'متابعة الأرباح',
    'التقارير',
    'الإعدادات',
  ];

  return (
    <div className="min-h-screen bg-black text-white flex flex-row-reverse">
      <aside className="w-72 bg-zinc-950 border-l border-zinc-800 p-5 hidden md:block">
        <h1 className="text-3xl font-bold text-blue-500 mb-8 text-center">
          Smart House ERP
        </h1>

        <div className="space-y-3">
          {menu.map((item, index) => (
            <div
              key={index}
              className="bg-zinc-900 hover:bg-blue-600 transition rounded-2xl p-4 cursor-pointer text-lg"
            >
              {item}
            </div>
          ))}
        </div>

        <div className="mt-10 bg-zinc-900 rounded-2xl p-4 text-center">
          <p className="text-zinc-400">المستخدم الحالي</p>
          <h2 className="text-xl font-bold mt-2">سمارت هاوس</h2>
        </div>
      </aside>

      <main className="flex-1 p-5">
        <div className="flex justify-between items-center mb-8">
          <div>
            <h2 className="text-4xl font-bold">إدارة العمل</h2>
            <p className="text-zinc-400 mt-2">
              متابعة المبيعات والخدمات والأرباح اليومية
            </p>
          </div>

          <button className="bg-blue-600 hover:bg-blue-700 px-5 py-3 rounded-2xl text-lg">
            إضافة عملية جديدة
          </button>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-5">
          {cards.map((card, index) => (
            <div
              key={index}
              className="bg-zinc-950 border border-zinc-800 rounded-3xl p-6 shadow-xl"
            >
              <div className="flex justify-between items-center">
                <span className="text-4xl">{card.icon}</span>
                <span className="text-zinc-400">اليوم</span>
              </div>

              <h3 className="text-2xl font-bold mt-6">{card.title}</h3>
              <p className="text-3xl text-blue-500 mt-4">{card.value}</p>
            </div>
          ))}
        </div>

        <div className="mt-10 grid grid-cols-1 xl:grid-cols-2 gap-5">
          <div className="bg-zinc-950 border border-zinc-800 rounded-3xl p-6">
            <h3 className="text-2xl font-bold mb-5">آخر العمليات</h3>

            <div className="space-y-4">
              <div className="bg-zinc-900 p-4 rounded-2xl flex justify-between">
                <span>إيداع فودافون كاش</span>
                <span className="text-green-400">+500 ج</span>
              </div>

              <div className="bg-zinc-900 p-4 rounded-2xl flex justify-between">
                <span>تصوير 4×6</span>
                <span className="text-blue-400">+80 ج</span>
              </div>

              <div className="bg-zinc-900 p-4 rounded-2xl flex justify-between">
                <span>صيانة هاتف</span>
                <span className="text-yellow-400">+250 ج</span>
              </div>
            </div>
          </div>

          <div className="bg-zinc-950 border border-zinc-800 rounded-3xl p-6">
            <h3 className="text-2xl font-bold mb-5">معلومات المحل</h3>

            <div className="space-y-4 text-lg">
              <p>📍 أمام مدرسة كفرهورين الإعدادية</p>
              <p>📞 01019588860</p>
              <p>🕑 من 2 ظهراً حتى 11:30 مساءً</p>
              <p>💼 خدمات: فوري - تصوير - صيانة - محافظ إلكترونية</p>
            </div>
          </div>
        </div>
      </main>
    </div>
  );
}
