---
title: コンポーネント サービスでのビジネス オブジェクトの実行
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309207"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="6d16a-102">コンポーネント サービスでのビジネス オブジェクトの実行</span><span class="sxs-lookup"><span data-stu-id="6d16a-102">Running business objects in component services</span></span>

<span data-ttu-id="6d16a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d16a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d16a-p101">ビジネス オブジェクトには、実行可能ファイル (.exe) とダイナミック リンク ライブラリ (.dll) があります。ビジネス オブジェクトを実行するために使う構成は、そのオブジェクトが .dll ファイルであるか .exe ファイルであるかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6d16a-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

- <span data-ttu-id="6d16a-p102">.exe ファイルとして作成されたビジネス オブジェクトは、DCOM を介して呼び出すことができます。これらのビジネス オブジェクトがインターネット インフォメーション サービス (IIS) を介して使用される場合は、データの追加マーシャリングの対象となるため、クライアントのパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="6d16a-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

- <span data-ttu-id="6d16a-p103">.dll ファイルとして作成されたビジネス オブジェクトは、IIS (したがって HTTP) を介して利用できます。また、コンポーネント サービス (Windows NT を使用している場合は Microsoft Transaction Server) を介する場合のみ、DCOM からも利用できます。IIS を介してアクセスできるようにするには、IIS サーバー コンピューターにビジネス オブジェクト DLL を登録する必要があります。DCOM で DLL を実行するための構成方法の手順については、「[DCOM で DLL を実行できるようにする](enabling-a-dll-to-run-on-dcom.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d16a-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="6d16a-112">中間層のビジネスオブジェクトがコンポーネントサービスコンポーネント ( **getobjectcontext**、 **SetComplete**、および**SetAbort**を使用) として実装されている場合は、コンポーネントサービス (または、Windows NT を使用している場合は MTS) を使用して、コンテキストオブジェクトを複数のクライアント呼び出し間で状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="6d16a-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="6d16a-113">このシナリオは、通常は信頼関係のあるクライアントとサーバー (イントラネット) 間で実装される DCOM でも可能です。</span><span class="sxs-lookup"><span data-stu-id="6d16a-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="6d16a-114">その場合、クライアント側の [RDS.DataSpace](dataspace-object-rds.md) オブジェクトと [CreateObject](createobject-method-rds.md) メソッドはトランザクション コンテキスト オブジェクトと **CreateInstance** メソッド ( **ITransactionContext** インターフェイスによって提供) に置き換えられ、コンポーネント サービスによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6d16a-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="6d16a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d16a-115">See also</span></span>

- [<span data-ttu-id="6d16a-116">コンポーネントサービスでのビジネスオブジェクトの実行 (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="6d16a-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
