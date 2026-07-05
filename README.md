import numpy as np
import matplotlib.pyplot as plt

# একটি ফিগার ও এক্সিস তৈরি (সাইজ ৬x৬ ইঞ্চি)
fig, ax = plt.subplots(figsize=(6, 6))

# হার্ট শেপের গাণিতিক সমীকরণ (Heart Equation)
t = np.linspace(0, 2 * np.pi, 1000)
x = 16 * np.sin(t)**3
y = 13 * np.cos(t) - 5 * np.cos(2*t) - 2 * np.cos(3*t) - np.cos(4*t)

# মন বা হার্টের রঙ (Pinkish Red) এবং বর্ডার সেট করা
ax.fill(x, y, color='#ff4d6d', edgecolor='#c9184a', linewidth=3)

# মনের ঠিক মাঝখানে "Rahat Hossain" নামটি বসানো
ax.text(0, 0, 'Rahat Hossain', fontsize=22, color='white', 
        weight='bold', ha='center', va='center', fontname='sans-serif')

# চারপাশের এক্সিস বা গ্রিড লাইনগুলো লুকিয়ে ফেলা
ax.axis('off')

# ছবিটি 'heart_rahat.png' নামে হাই-কোয়ালিটিতে সেভ করা
plt.savefig('heart_rahat.png', bbox_inches='tight', dpi=300, transparent=True)

# ডিসপ্লেতে দেখানোর জন্য
plt.show()
