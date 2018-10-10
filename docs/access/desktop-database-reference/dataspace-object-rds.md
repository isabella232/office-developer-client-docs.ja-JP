---
title: DataSpace オブジェクト (RDS)
TOCTitle: DataSpace Object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2466727f52a37d396e7478fa54d27a68158855a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476614"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="38c33-102">DataSpace オブジェクト (RDS)</span><span class="sxs-lookup"><span data-stu-id="38c33-102">DataSpace Object (RDS)</span></span>

<span data-ttu-id="38c33-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="38c33-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="38c33-104">中間層にあるカスタム ビジネス オブジェクトにクライアント側プロキシを作成します。</span><span class="sxs-lookup"><span data-stu-id="38c33-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c33-105">備考</span><span class="sxs-lookup"><span data-stu-id="38c33-105">Remarks</span></span>

<span data-ttu-id="38c33-p101">リモート データ サービスでは、クライアント側コンポーネントが中間層にあるビジネス オブジェクトと通信するために、ビジネス オブジェクト プロキシが必要となります。プロキシは、プロセスまたはマシンの境界を越えて、アプリケーションの [Recordset](recordset-object-ado.md) データを簡単にパッケージ化したり、パッケージ化を解除したり、送信 (マーシャリング) したりできます。</span><span class="sxs-lookup"><span data-stu-id="38c33-p101">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier. Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="38c33-p102">リモート データ サービスは、 **RDS.DataSpace** オブジェクトの [CreateObject](createobject-method-rds.md) メソッドを使用して、ビジネス オブジェクト プロキシを作成します。ビジネス オブジェクト プロキシは、中間層のビジネス オブジェクトの相手方のインスタンスが作成されるたびに動的に作成されます。リモート データ サービスは、HTTP、HTTPS (HTTP Secure Sockets)、DCOM、およびインプロセス (クライアント コンポーネントとビジネス オブジェクトが同じコンピューター上に常駐している) の各プロトコルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38c33-p102">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies. The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created. Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="38c33-p103">[!メモ] **RDS.DataSpace** オブジェクトが HTTP プロトコルまたは HTTPS プロトコルを使用している場合、RDS は "状態のない" 形で動作します。つまり、クライアント要求に関する内部情報は、サーバーが応答を返した後破棄されます。</span><span class="sxs-lookup"><span data-stu-id="38c33-p103">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols. That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="38c33-p104">ビジネス オブジェクトは、ビジネス オブジェクト プロキシの存続期間中は存在しているように見えますが、実際には要求に対して応答を送信するまでの間しか存在しません。要求を発行すると (つまり、ビジネス オブジェクト上でメソッドを呼び出すと)、プロキシはサーバーへの新しい接続を開き、サーバーはビジネス オブジェクトの新しいインスタンスを作成します。ビジネス オブジェクトが要求に応答後、サーバーはビジネス オブジェクトを破棄し、接続を閉じます。</span><span class="sxs-lookup"><span data-stu-id="38c33-p104">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request. When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object. After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="38c33-p105">この動作から、ビジネス オブジェクト プロパティまたは変数を使用してデータを要求間で渡すことができないことがわかります。状態データを保持するには、ファイルやメソッドの引数など、別の機能を採用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38c33-p105">This behavior means you cannot pass data from one request to another using a business object property or variable. You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="38c33-118">**RDS.DataSpace** オブジェクトのクラス ID は、BD96C556-65A3-11D0-983A-00C04FC29E36 です。</span><span class="sxs-lookup"><span data-stu-id="38c33-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>

