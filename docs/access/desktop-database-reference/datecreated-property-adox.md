---
title: DateCreated プロパティ (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 962c5e00eee3c58d2c02040869fdf1cb454af538
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478570"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="72625-102">DateCreated プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="72625-102">DateCreated Property (ADOX)</span></span>


<span data-ttu-id="72625-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="72625-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72625-104">オブジェクトが作成された日付を示します。</span><span class="sxs-lookup"><span data-stu-id="72625-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="72625-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="72625-105">Return Values</span></span>

<span data-ttu-id="72625-p101">作成された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateCreated** をサポートしていない場合、値は Null 値になります。</span><span class="sxs-lookup"><span data-stu-id="72625-p101">Returns a **Variant** value specifying the date created. The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="72625-108">解説</span><span class="sxs-lookup"><span data-stu-id="72625-108">Remarks</span></span>

<span data-ttu-id="72625-p102">新しく追加されたオブジェクトの **DateCreated** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、 [DateCreated](refresh-method-ado.md) プロパティの値を取得するには、 [Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの **Refresh** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="72625-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

