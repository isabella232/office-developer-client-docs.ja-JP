---
title: DateModified プロパティ (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceafd13b33536a77a1d793e7167fe8042609be5e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603330"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="643c1-102">DateModified プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="643c1-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="643c1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="643c1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="643c1-104">オブジェクトが最後に変更された日付を示します。</span><span class="sxs-lookup"><span data-stu-id="643c1-104">Indicates the date the object was last modified.</span></span>

<span data-ttu-id="643c1-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="643c1-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="643c1-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="643c1-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="643c1-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="643c1-107">Return values</span></span>
>>>>>>> <span data-ttu-id="643c1-108">master</span><span class="sxs-lookup"><span data-stu-id="643c1-108">master</span></span>

<span data-ttu-id="643c1-p101">変更された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateModified** をサポートしていない場合、値は Null 値になります。</span><span class="sxs-lookup"><span data-stu-id="643c1-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="643c1-111">解説</span><span class="sxs-lookup"><span data-stu-id="643c1-111">Remarks</span></span>

<span data-ttu-id="643c1-p102">新しく追加されたオブジェクトの **DateModified** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、 [DateModified](refresh-method-ado.md) プロパティの値を取得するには、 [Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの **Refresh** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="643c1-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

