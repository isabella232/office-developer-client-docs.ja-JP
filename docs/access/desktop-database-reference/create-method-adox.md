---
title: Create メソッド (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295423"
---
# <a name="create-method-adox"></a><span data-ttu-id="79e28-102">Create メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="79e28-102">Create method (ADOX)</span></span>

<span data-ttu-id="79e28-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="79e28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79e28-104">新規カタログを作成します。</span><span class="sxs-lookup"><span data-stu-id="79e28-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e28-105">構文</span><span class="sxs-lookup"><span data-stu-id="79e28-105">Syntax</span></span>

<span data-ttu-id="79e28-106">*カタログ*。*connectstring*を作成する</span><span class="sxs-lookup"><span data-stu-id="79e28-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="79e28-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79e28-107">Parameters</span></span>

|<span data-ttu-id="79e28-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79e28-108">Parameter</span></span>|<span data-ttu-id="79e28-109">説明</span><span class="sxs-lookup"><span data-stu-id="79e28-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="79e28-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="79e28-110">*ConnectString*</span></span> |<span data-ttu-id="79e28-111">データ ソースとの接続に使用される文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="79e28-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="79e28-112">注釈</span><span class="sxs-lookup"><span data-stu-id="79e28-112">Remarks</span></span>

<span data-ttu-id="79e28-p101">**Create** メソッドは、*ConnectString* で指定したデータ ソースへの新しい ADO [Connection](connection-object-ado.md) を作成して開きます。成功すると、新しい **Connection** オブジェクトが [ActiveConnection](activeconnection-property-adox.md) プロパティに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="79e28-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="79e28-115">プロバイダーが新しいカタログの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="79e28-115">An error will occur if the provider does not support creating new catalogs.</span></span>

