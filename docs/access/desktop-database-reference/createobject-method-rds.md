---
title: CreateObject メソッド (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d08b596afb24fff430c6c662a557da1880addefa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921181"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="43d54-102">CreateObject メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="43d54-102">CreateObject method (RDS)</span></span>


<span data-ttu-id="43d54-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="43d54-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="43d54-p101">目的のビジネス オブジェクトのプロキシを作成し、そのポインターを返します。プロキシは、インターネット上で要求やデータを送信するビジネス オブジェクトと交信するために、データをパッケージ化し、サーバー側スタブにマーシャリングします。インプロセス コンポーネント オブジェクトでは、プロキシは使用されず、オブジェクトへのポインターのみが返されます。</span><span class="sxs-lookup"><span data-stu-id="43d54-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d54-107">構文</span><span class="sxs-lookup"><span data-stu-id="43d54-107">Syntax</span></span>

<span data-ttu-id="43d54-108">RDS は、HTTP、HTTPS (HTTP over Secure Socket Layer)、DCOM、およびインプロセスのプロトコルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="43d54-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43d54-109">プロトコル</span><span class="sxs-lookup"><span data-stu-id="43d54-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="43d54-110">構文</span><span class="sxs-lookup"><span data-stu-id="43d54-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43d54-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="43d54-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="43d54-112"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="43d54-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d54-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="43d54-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="43d54-114"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="43d54-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43d54-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="43d54-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="43d54-116"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot;<em>コンピューター名</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="43d54-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d54-117">インプロセス</span><span class="sxs-lookup"><span data-stu-id="43d54-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="43d54-118"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="43d54-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="43d54-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43d54-119">Parameters</span></span>

  - <span data-ttu-id="43d54-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="43d54-120">*Object*</span></span>

  - <span data-ttu-id="43d54-121">*ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="43d54-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="43d54-122">*インスタンス*</span><span class="sxs-lookup"><span data-stu-id="43d54-122">*DataSpace*</span></span>

  - <span data-ttu-id="43d54-123">新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="43d54-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="43d54-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="43d54-124">*ProgID*</span></span>

  - <span data-ttu-id="43d54-125">アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="43d54-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="43d54-126">*awebsrvr*または*コンピューター名*</span><span class="sxs-lookup"><span data-stu-id="43d54-126">*awebsrvr* or *computername*</span></span>

  - <span data-ttu-id="43d54-127">サーバー ビジネス オブジェクトのインスタンスを作成する、インターネット インフォメーション サービス (IIS) web サーバーを識別する URL を表す**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="43d54-127">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d54-128">備考</span><span class="sxs-lookup"><span data-stu-id="43d54-128">Remarks</span></span>

<span data-ttu-id="43d54-129">*HTTP プロトコル*は、標準の web プロトコルです。*HTTPS*は、セキュリティで保護された web プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="43d54-129">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="43d54-130">HTTP なしのローカル ・ エリア ・ ネットワークを実行している場合は、 *DCOM プロトコル*を使用します。</span><span class="sxs-lookup"><span data-stu-id="43d54-130">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="43d54-131">*プロセス内*のプロトコルは、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークを使用しません。</span><span class="sxs-lookup"><span data-stu-id="43d54-131">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

