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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297096"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="c98a5-102">Append メソッド (ADOX Indexes)</span><span class="sxs-lookup"><span data-stu-id="c98a5-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="c98a5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c98a5-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="c98a5-104">新しい [Index](index-object-adox.md) オブジェクトを [Indexes](indexes-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="c98a5-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c98a5-105">構文</span><span class="sxs-lookup"><span data-stu-id="c98a5-105">Syntax</span></span>

<span data-ttu-id="c98a5-106">*インデックス*。追加*インデックス* \[、*列*\]</span><span class="sxs-lookup"><span data-stu-id="c98a5-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c98a5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c98a5-107">Parameters</span></span>

|<span data-ttu-id="c98a5-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c98a5-108">Parameter</span></span>|<span data-ttu-id="c98a5-109">説明</span><span class="sxs-lookup"><span data-stu-id="c98a5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c98a5-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c98a5-110">*Index*</span></span> |<span data-ttu-id="c98a5-111">追加する **Index** オブジェクトを指定します。または、新たに作成して追加するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c98a5-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="c98a5-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="c98a5-112">*Columns*</span></span> |<span data-ttu-id="c98a5-p101">省略可能です。インデックスが作成される列の名前を示すバリアント型 (**Variant**) の値を指定します。*Columns* パラメーターは、1 つ以上の [Column](column-object-adox.md) オブジェクトの [Name](name-property-adox.md) プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="c98a5-p101">Optional. A **Variant** value that specifies the name(s) of the column(s) to be indexed. The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c98a5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c98a5-116">Remarks</span></span>

<span data-ttu-id="c98a5-117">*Columns* パラメーターは、列の名前または列の名前の配列のいずれかとなります。</span><span class="sxs-lookup"><span data-stu-id="c98a5-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="c98a5-118">プロバイダーがインデックスの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c98a5-118">An error will occur if the provider does not support creating indexes.</span></span>

