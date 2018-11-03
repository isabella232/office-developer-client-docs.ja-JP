---
title: Name プロパティ (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931247"
---
# <a name="name-property-adox"></a><span data-ttu-id="f6195-102">Name プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f6195-102">Name property (ADOX)</span></span>


<span data-ttu-id="f6195-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f6195-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6195-104">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="f6195-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f6195-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="f6195-105">Settings and return values</span></span>

<span data-ttu-id="f6195-106">文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="f6195-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6195-107">解説</span><span class="sxs-lookup"><span data-stu-id="f6195-107">Remarks</span></span>

<span data-ttu-id="f6195-108">名前は、コレクション内で一意である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f6195-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="f6195-p101">**Name** プロパティは、 [Column](column-object-adox.md)、[Group](group-object-adox.md)、[Key](key-object-adox.md)、[Index](index-object-adox.md)、[Table](table-object-adox.md)、および [User](user-object-adox.md) オブジェクトでは、値の取得および設定が可能です。 **Name** プロパティは、 [Catalog](catalog-object-adox.md)、[Procedure](procedure-object-adox.md)、および [View](view-object-adox.md) オブジェクトでは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="f6195-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="f6195-111">値の取得および設定が可能なオブジェクト (**Column**、**Group**、**Key**、**Index**、**Table**、および **User** オブジェクト) では、既定値は空の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="f6195-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="f6195-112">[!メモ] キーの場合、このプロパティは、既にコレクションに追加されている <STRONG>Key</STRONG> オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="f6195-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="f6195-113">[!メモ] テーブルの場合、このプロパティは、既にコレクションに追加されている <STRONG>Table</STRONG> オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="f6195-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


