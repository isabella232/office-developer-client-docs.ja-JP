---
title: datecreated プロパティプロパティ (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294422"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="d0d4c-102">datecreated プロパティプロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d0d4c-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="d0d4c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0d4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0d4c-104">オブジェクトが作成された日付を示します。</span><span class="sxs-lookup"><span data-stu-id="d0d4c-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0d4c-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="d0d4c-105">Return values</span></span>

<span data-ttu-id="d0d4c-106">作成された日付を示すバリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="d0d4c-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="d0d4c-107">プロバイダーが **DateCreated** をサポートしていない場合、値は Null 値になります。</span><span class="sxs-lookup"><span data-stu-id="d0d4c-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0d4c-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d0d4c-108">Remarks</span></span>

<span data-ttu-id="d0d4c-p102">新しく追加されたオブジェクトの **DateCreated** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、**DateCreated** プロパティの値を取得するには、[Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの [Refresh](refresh-method-ado.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0d4c-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

