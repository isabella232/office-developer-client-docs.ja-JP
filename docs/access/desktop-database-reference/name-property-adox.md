---
title: Name プロパティ (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604051"
---
# <a name="name-property-adox"></a><span data-ttu-id="2aec3-102">Name プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2aec3-102">Name Property (ADOX)</span></span>


<span data-ttu-id="2aec3-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2aec3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2aec3-104">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-104">Indicates the name of the object.</span></span>

<span data-ttu-id="2aec3-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="2aec3-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2aec3-106">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="2aec3-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2aec3-107">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="2aec3-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2aec3-108">master</span><span class="sxs-lookup"><span data-stu-id="2aec3-108">master</span></span>

<span data-ttu-id="2aec3-109">文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-109">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aec3-110">解説</span><span class="sxs-lookup"><span data-stu-id="2aec3-110">Remarks</span></span>

<span data-ttu-id="2aec3-111">名前は、コレクション内で一意である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2aec3-111">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="2aec3-p101">**Name** プロパティは、 [Column](column-object-adox.md)、[Group](group-object-adox.md)、[Key](key-object-adox.md)、[Index](index-object-adox.md)、[Table](table-object-adox.md)、および [User](user-object-adox.md) オブジェクトでは、値の取得および設定が可能です。 **Name** プロパティは、 [Catalog](catalog-object-adox.md)、[Procedure](procedure-object-adox.md)、および [View](view-object-adox.md) オブジェクトでは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="2aec3-114">値の取得および設定が可能なオブジェクト (**Column**、**Group**、**Key**、**Index**、**Table**、および **User** オブジェクト) では、既定値は空の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-114">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="2aec3-115">[!メモ] キーの場合、このプロパティは、既にコレクションに追加されている <STRONG>Key</STRONG> オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-115">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="2aec3-116">[!メモ] テーブルの場合、このプロパティは、既にコレクションに追加されている <STRONG>Table</STRONG> オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-116">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


