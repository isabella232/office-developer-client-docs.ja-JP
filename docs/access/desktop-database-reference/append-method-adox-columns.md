---
title: Append メソッド (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877661"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="0cd3a-102">Append メソッド (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="0cd3a-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="0cd3a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0cd3a-104">新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd3a-105">構文</span><span class="sxs-lookup"><span data-stu-id="0cd3a-105">Syntax</span></span>

<span data-ttu-id="0cd3a-106">*列*です。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-106">*Columns*.</span></span> <span data-ttu-id="0cd3a-107">*列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="0cd3a-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0cd3a-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0cd3a-108">Parameters</span></span>

  - <span data-ttu-id="0cd3a-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="0cd3a-109">*Column*</span></span>

  - <span data-ttu-id="0cd3a-110">追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="0cd3a-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="0cd3a-111">*Type*</span></span>

  - <span data-ttu-id="0cd3a-112">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-112">Optional.</span></span> <span data-ttu-id="0cd3a-113">列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="0cd3a-114">*型*パラメーターは、**列**オブジェクトの[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="0cd3a-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="0cd3a-115">*DefinedSize*</span></span>

  - <span data-ttu-id="0cd3a-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-116">Optional.</span></span> <span data-ttu-id="0cd3a-117">列のサイズを指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="0cd3a-118">*DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="0cd3a-119">[!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0cd3a-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


