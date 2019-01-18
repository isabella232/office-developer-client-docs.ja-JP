---
title: Append メソッド (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707557"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="93042-102">Append メソッド (ADOX Indexes)</span><span class="sxs-lookup"><span data-stu-id="93042-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="93042-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="93042-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="93042-104">新しい [Index](index-object-adox.md) オブジェクトを [Indexes](indexes-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="93042-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="93042-105">構文</span><span class="sxs-lookup"><span data-stu-id="93042-105">Syntax</span></span>

<span data-ttu-id="93042-106">*インデックス*です。*インデックス*を追加する\[、*列*\]</span><span class="sxs-lookup"><span data-stu-id="93042-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="93042-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93042-107">Parameters</span></span>

|<span data-ttu-id="93042-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93042-108">Parameter</span></span>|<span data-ttu-id="93042-109">説明</span><span class="sxs-lookup"><span data-stu-id="93042-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="93042-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="93042-110">*Index*</span></span> |<span data-ttu-id="93042-111">追加する **Index** オブジェクトを指定します。または、新たに作成して追加するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93042-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="93042-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="93042-112">*Columns*</span></span> |<span data-ttu-id="93042-113">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="93042-113">Optional.</span></span> <span data-ttu-id="93042-114">インデックスが作成される列の名前を示すバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="93042-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="93042-115">*Columns*パラメーターは、[列](column-object-adox.md)オブジェクトまたはオブジェクトの[Name](name-property-adox.md)プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="93042-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="93042-116">注釈</span><span class="sxs-lookup"><span data-stu-id="93042-116">Remarks</span></span>

<span data-ttu-id="93042-117">*Columns*パラメーターには、列の名前または列名の配列のいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="93042-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="93042-118">プロバイダーがインデックスの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="93042-118">An error will occur if the provider does not support creating indexes.</span></span>

