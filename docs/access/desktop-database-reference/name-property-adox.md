---
title: Name プロパティ (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707984"
---
# <a name="name-property-adox"></a><span data-ttu-id="e78a6-102">Name プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e78a6-102">Name property (ADOX)</span></span>

<span data-ttu-id="e78a6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e78a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e78a6-104">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="e78a6-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e78a6-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="e78a6-105">Settings and return values</span></span>

<span data-ttu-id="e78a6-106">文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="e78a6-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e78a6-107">解説</span><span class="sxs-lookup"><span data-stu-id="e78a6-107">Remarks</span></span>

<span data-ttu-id="e78a6-108">名前は、コレクション内で一意である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e78a6-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="e78a6-p101">**Name** プロパティは、 [Column](column-object-adox.md)、[Group](group-object-adox.md)、[Key](key-object-adox.md)、[Index](index-object-adox.md)、[Table](table-object-adox.md)、および [User](user-object-adox.md) オブジェクトでは、値の取得および設定が可能です。 **Name** プロパティは、 [Catalog](catalog-object-adox.md)、[Procedure](procedure-object-adox.md)、および [View](view-object-adox.md) オブジェクトでは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e78a6-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="e78a6-111">値の取得および設定が可能なオブジェクト (**Column**、**Group**、**Key**、**Index**、**Table**、および **User** オブジェクト) では、既定値は空の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="e78a6-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="e78a6-112">[!メモ] キーの場合、このプロパティは、既にコレクションに追加されている **Key** オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e78a6-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="e78a6-113">[!メモ] テーブルの場合、このプロパティは、既にコレクションに追加されている **Table** オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e78a6-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


