---
title: Server プロパティ (RDS)
TOCTitle: Server Property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 487b6e676816ab571cb08f6cfe7870362c7a8c84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868435"
---
# <a name="server-property-rds"></a><span data-ttu-id="baf05-102">Server プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="baf05-102">Server Property (RDS)</span></span>


<span data-ttu-id="baf05-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="baf05-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baf05-104">インターネット インフォメーション サービス (IIS) 名および通信プロトコルを示します。</span><span class="sxs-lookup"><span data-stu-id="baf05-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="baf05-105">**Server** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。</span><span class="sxs-lookup"><span data-stu-id="baf05-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf05-106">構文</span><span class="sxs-lookup"><span data-stu-id="baf05-106">Syntax</span></span>

|<span data-ttu-id="baf05-107">プロトコル</span><span class="sxs-lookup"><span data-stu-id="baf05-107">Protocol</span></span>|<span data-ttu-id="baf05-108">デザイン時の構文</span><span class="sxs-lookup"><span data-stu-id="baf05-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="baf05-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="baf05-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="baf05-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="baf05-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="baf05-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="baf05-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="baf05-112">インプロセス</span><span class="sxs-lookup"><span data-stu-id="baf05-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="baf05-113">プロトコル</span><span class="sxs-lookup"><span data-stu-id="baf05-113">Protocol</span></span>|<span data-ttu-id="baf05-114">実行時の構文</span><span class="sxs-lookup"><span data-stu-id="baf05-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="baf05-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="baf05-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="baf05-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="baf05-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="baf05-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="baf05-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="baf05-118">インプロセス</span><span class="sxs-lookup"><span data-stu-id="baf05-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="baf05-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="baf05-119">Parameters</span></span>

<span data-ttu-id="baf05-120">*awebsrvr*または*コンピューター名*</span><span class="sxs-lookup"><span data-stu-id="baf05-120">*awebsrvr* or *computername*</span></span>

- <span data-ttu-id="baf05-121">サーバーがリモート コンピューター上にある場合は、インターネット パス、イントラネット パス、またはコンピューター名を含む文字列型 ( **String** ) の値。サーバーがローカル コンピューター上にある場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="baf05-121">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>

<span data-ttu-id="baf05-122">*port*</span><span class="sxs-lookup"><span data-stu-id="baf05-122">*port*</span></span>

- <span data-ttu-id="baf05-123">省略可能。</span><span class="sxs-lookup"><span data-stu-id="baf05-123">Optional.</span></span> <span data-ttu-id="baf05-124">IIS サーバーへの接続に使用されるポートです。</span><span class="sxs-lookup"><span data-stu-id="baf05-124">A port that is used to connect to an IIS server.</span></span> <span data-ttu-id="baf05-125">Internet Explorer で、ポート番号を設定 ([**ツール**] メニューで、 **[インターネット オプション**] をクリックし、[**接続**] タブを選択し、) または IIS で。</span><span class="sxs-lookup"><span data-stu-id="baf05-125">The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>

<span data-ttu-id="baf05-126">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="baf05-126">*DataControl*</span></span>

- <span data-ttu-id="baf05-127">**RDS.DataControl** オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="baf05-127">An object variable that represents an **RDS.DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="baf05-128">解説</span><span class="sxs-lookup"><span data-stu-id="baf05-128">Remarks</span></span>

<span data-ttu-id="baf05-129">サーバーは、 **RDS.DataControl** 要求 (クエリまたは更新) が処理される場所です。</span><span class="sxs-lookup"><span data-stu-id="baf05-129">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="baf05-130">既定では、すべての要求は指定されたサーバー上の [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクト、 [MSDFMAP.Handler](datafactory-customization.md) コンポーネント、および [MSDFMAP.INI](understanding-the-customization-file.md) ファイルによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="baf05-130">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="baf05-131">サーバーを変更する場合は、新旧の **MSDFMAP.INI** ファイルの設定を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="baf05-131">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="baf05-132">互換性がないと、一方のサーバーで成功した要求が、もう一方のサーバーでは失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="baf05-132">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="baf05-133">Server プロパティが "" に設定されている場合、これらのオブジェクトはローカル コンピューターで使用されます。</span><span class="sxs-lookup"><span data-stu-id="baf05-133">If the Server property is set to "", these objects will be used on the local machine.</span></span>

