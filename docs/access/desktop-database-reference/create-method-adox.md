---
title: Create メソッド (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01f45adaf5bdd15841be86bfea62cca58e21a9d9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925517"
---
# <a name="create-method-adox"></a><span data-ttu-id="92e77-102">Create メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="92e77-102">Create method (ADOX)</span></span>


<span data-ttu-id="92e77-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="92e77-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="92e77-104">新規カタログを作成します。</span><span class="sxs-lookup"><span data-stu-id="92e77-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e77-105">構文</span><span class="sxs-lookup"><span data-stu-id="92e77-105">Syntax</span></span>

<span data-ttu-id="92e77-106">*カタログ*です。*あわせて*を作成します。</span><span class="sxs-lookup"><span data-stu-id="92e77-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="92e77-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92e77-107">Parameters</span></span>

  - <span data-ttu-id="92e77-108">*あわせて*</span><span class="sxs-lookup"><span data-stu-id="92e77-108">*ConnectString*</span></span>

  - <span data-ttu-id="92e77-109">データ ソースとの接続に使用される文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="92e77-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="92e77-110">解説</span><span class="sxs-lookup"><span data-stu-id="92e77-110">Remarks</span></span>

<span data-ttu-id="92e77-p101">**Create** メソッドは、*ConnectString* で指定したデータ ソースへの新しい ADO [Connection](connection-object-ado.md) を作成して開きます。成功すると、新しい **Connection** オブジェクトが [ActiveConnection](activeconnection-property-adox.md) プロパティに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="92e77-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="92e77-113">プロバイダーが新しいカタログの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="92e77-113">An error will occur if the provider does not support creating new catalogs.</span></span>

