---
title: Append メソッド (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297124"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="01812-102">Append メソッド (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="01812-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="01812-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="01812-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01812-104">新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="01812-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="01812-105">構文</span><span class="sxs-lookup"><span data-stu-id="01812-105">Syntax</span></span>

<span data-ttu-id="01812-106">*列*。</span><span class="sxs-lookup"><span data-stu-id="01812-106">*Columns*.</span></span> <span data-ttu-id="01812-107">*列* \[、*型*\] \*\* 、および未定義のサイズを追加する\[\]</span><span class="sxs-lookup"><span data-stu-id="01812-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="01812-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01812-108">Parameters</span></span>

|<span data-ttu-id="01812-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01812-109">Parameter</span></span>|<span data-ttu-id="01812-110">説明</span><span class="sxs-lookup"><span data-stu-id="01812-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="01812-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="01812-111">*Column*</span></span> |<span data-ttu-id="01812-112">追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="01812-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="01812-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="01812-113">*Type*</span></span> |<span data-ttu-id="01812-p102">省略可能です。列のデータ型を指定する長整数型 (**Long**) の値を指定します。*Type* パラメーターは、**Column** オブジェクトの [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="01812-p102">Optional. A **Long** value that specifies the data type of the column. The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="01812-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="01812-117">*DefinedSize*</span></span> |<span data-ttu-id="01812-118">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="01812-118">Optional.</span></span> <span data-ttu-id="01812-119">列のサイズを指定する長整数型 (**Long**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="01812-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="01812-120">*DefinedSize* パラメーターは、**Column** オブジェクトの [DefinedSize](definedsize-property-adox.md) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="01812-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="01812-121">**Column** を [Index](index-object-adox.md) の **Columns** コレクションに追加するときに、[Tables](tables-collection-adox.md) コレクションに既に追加されている [Table](table-object-adox.md) にまだ **Column** が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="01812-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


