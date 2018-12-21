# Снимки дисков

_Снимок диска_ в Яндекс.Облаке — это копия файловой системы диска на определенный момент времени.

Вы можете использовать снимки для различных целей, например:

- перенос данных с одного диска на другой — например, на диск в другой зоне доступности;
- создание резервной копии диска перед проведением операций, которые могут повлечь повреждение данных;
- версионирование диска путем регулярного создания снимков диска.

> [!NOTE]
>
> Если вам надо создавать много дисков с одинаковым содержимым, используйте [образы](images.md). Создание диска из образа происходит быстрее, чем из снимка.

## Снимок диска как ресурс Яндекс.Облака {#concept_pdw_xtc_v2b}

Снимок диска является таким же ресурсом, как и сам диск. Снимок создается в каталоге. Права доступа к снимку наследуются от прав доступа к каталогу.

Снимок занимает место в хранилище, и хранение снимков оплачивается дополнительно. Подробнее читайте в разделе [[!TITLE]](../pricing.md).

В информации о снимке содержится идентификатор диска, из которого он был создан. Помимо этого от ресурса-источника наследуется идентификаторы лицензий (`product_ids`), которые используются при расчете стоимости использования диска.

## Резервное копирование {#backup}

Каждый снимок автоматически реплицируется в нескольких зонах доступности — таким образом обеспечивается надежность хранения данных.