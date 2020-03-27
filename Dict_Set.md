Словарь (dict) оформляется фигурными скобками. Его
заполняют пары, записанные через запятую. Первый
элемент в паре называется ключ, а второй — значение,
они разделяются между собой двоеточием.

english = {
  'рука': 'hand',
  'нога': 'leg',
  'разработчик': 'developer'
}

# доступ по ключу: как по-английски рука?
print(english['рука'])
english['рука'] = 'arm'

# значение для ключа 'рука'
# поменялось с 'hand' на 'arm'

Пройти по всем элементам словаря можно циклом for, причём есть несколько вариантов:

favorite_songs = {
  'Тополиный пух': 'Иванушки international',
  'Город золотой': 'Аквариум',
  'Звезда по имени Солнце': 'Кино',
  'Группа крови': 'Кино'
}

for track in favorite_songs:
  print(track + ' это песня группы ' + favorite_songs[track])
for music_band in favorite_songs.values():
  print('Доктор, я больше не могу слушать группу ' + music_band)
for track, music_band in favorite_songs.items():
  print(track + ' это песня группы ' + music_band)
    
Метод .keys() возвращает все ключи словаря, а метод .values() — все значения


Множества

Тип set похож на список, но есть два важных отличия:

• элементы во множестве не повторяются;
• не гарантируется, что при выводе элементов на экран будет соблюден какой-то определённый порядок.

word_set = {'hand', 'leg', 'developer'}

# получаем сет unique_band_names
# (с англ. «уникальные названия групп»)

unique_band_names = set(bands)
for band in unique_band_names:
  print('Не могу больше слушать', band)

Метод .union() объединяет два множества:

songs1 = {
  'Три белых коня',
  'Happy new year',
  'Снежинка'
}
songs2 = {
  'Last christmas',
  'Снежинка',
  'Happy new year'
}
print(songs1.union(songs2))

# 'Три белых коня', 'Снежинка',
# 'Last christmas', 'Happy new year'

Проверка наличия элемента

if 'Аквариум' in unique_band_names:
  print('есть такое!')
if 'body' not in word_set:
  print('нету')
  
  
Метод .difference() возвращает разницу множеств, а
метод .intersection() — их пересечение.
