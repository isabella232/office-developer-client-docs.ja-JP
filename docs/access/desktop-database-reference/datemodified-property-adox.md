---
title: DateModified プロパティ (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7698534d0c77952cd116ea2e9b5726c3df758413
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889694"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="b0e7a-102">DateModified プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b0e7a-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="b0e7a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b0e7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0e7a-104">オブジェクトが最後に変更された日付を示します。</span><span class="sxs-lookup"><span data-stu-id="b0e7a-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0e7a-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="b0e7a-105">Return values</span></span>

<span data-ttu-id="b0e7a-p101">変更された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateModified** をサポートしていない場合、値は Null 値になります。</span><span class="sxs-lookup"><span data-stu-id="b0e7a-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e7a-108">解説</span><span class="sxs-lookup"><span data-stu-id="b0e7a-108">Remarks</span></span>

<span data-ttu-id="b0e7a-p102">新しく追加されたオブジェクトの **DateModified** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、 [DateModified](refresh-method-ado.md) プロパティの値を取得するには、 [Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの **Refresh** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e7a-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

