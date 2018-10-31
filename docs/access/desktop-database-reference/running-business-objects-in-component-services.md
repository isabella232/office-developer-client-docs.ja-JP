---
title: コンポーネント サービスでビジネス オブジェクトを実行する
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0eb70a615f49ff351ec31a826abc9775558218dd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862556"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="3d290-102">コンポーネント サービスでビジネス オブジェクトを実行する</span><span class="sxs-lookup"><span data-stu-id="3d290-102">Running Business Objects in Component Services</span></span>


<span data-ttu-id="3d290-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d290-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d290-p101">ビジネス オブジェクトには、実行可能ファイル (.exe) とダイナミック リンク ライブラリ (.dll) があります。ビジネス オブジェクトを実行するために使う構成は、そのオブジェクトが .dll ファイルであるか .exe ファイルであるかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3d290-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

  - <span data-ttu-id="3d290-p102">.exe ファイルとして作成されたビジネス オブジェクトは、DCOM を介して呼び出すことができます。これらのビジネス オブジェクトがインターネット インフォメーション サービス (IIS) を介して使用される場合は、データの追加マーシャリングの対象となるため、クライアントのパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="3d290-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

  - <span data-ttu-id="3d290-p103">.dll ファイルとして作成されたビジネス オブジェクトは、IIS (したがって HTTP) を介して利用できます。また、コンポーネント サービス (Windows NT を使用している場合は Microsoft Transaction Server) を介する場合のみ、DCOM からも利用できます。IIS を介してアクセスできるようにするには、IIS サーバー コンピューターにビジネス オブジェクト DLL を登録する必要があります。DCOM で DLL を実行するための構成方法の手順については、「[DCOM で DLL を実行できるようにする](enabling-a-dll-to-run-on-dcom.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d290-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="3d290-112">中間層のビジネス オブジェクトは、コンポーネント サービスのコンポーネント ( **GetObjectContext**、 **SetComplete**、および**SetAbort**を使用) として実装されているを使って、コンポーネント サービス (または Windows NT を使用している場合は MTS) コンテキスト オブジェクトを複数のクライアント呼び出し間で状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="3d290-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="3d290-113">このシナリオは、通常は信頼関係のあるクライアントとサーバー (イントラネット) 間で実装される DCOM でも可能です。</span><span class="sxs-lookup"><span data-stu-id="3d290-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="3d290-114">その場合、クライアント側の [RDS.DataSpace](dataspace-object-rds.md) オブジェクトと [CreateObject](createobject-method-rds.md) メソッドはトランザクション コンテキスト オブジェクトと **CreateInstance** メソッド ( **ITransactionContext** インターフェイスによって提供) に置き換えられ、コンポーネント サービスによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3d290-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="3d290-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d290-115">See also</span></span>

- [<span data-ttu-id="3d290-116">コンポーネント サービス (SQL Server) のビジネス オブジェクトを実行しています。</span><span class="sxs-lookup"><span data-stu-id="3d290-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)