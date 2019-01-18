---
title: DataFactory オブジェクト (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702181"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="34220-102">DataFactory オブジェクト (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="34220-102">DataFactory object (RDSServer)</span></span>


<span data-ttu-id="34220-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="34220-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34220-104">この既定のサーバー側ビジネス オブジェクトは、指定されたデータ ソースの読み取り/書き込みデータ アクセス権をクライアント側アプリケーションに提供するメソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="34220-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="34220-105">備考</span><span class="sxs-lookup"><span data-stu-id="34220-105">Remarks</span></span>

<span data-ttu-id="34220-106">**RDSServer.DataFactory** オブジェクトは、クライアント要求を受け取るサーバー側 Automation オブジェクトとして設計されています。</span><span class="sxs-lookup"><span data-stu-id="34220-106">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="34220-107">インターネット実装では、web サーバー上に常駐し、ADISAPI コンポーネントによってインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="34220-107">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="34220-108">**RDSServer.DataFactory** オブジェクトは、指定されたデータ ソースの読み取り/書き込みデータ アクセス権を提供しますが、検証やビジネス ルール ロジックの機能は搭載していません。</span><span class="sxs-lookup"><span data-stu-id="34220-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="34220-p102">**RDSServer.DataFactory** オブジェクトと [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの両方で使用できるメソッドを使用する場合、リモート データ サービスは既定で **RDS.DataControl** バージョンを使用します。既定では、 **RDSServer.DataFactory** が汎用のサーバー側ビジネス オブジェクトとして機能する、基本的なプログラミング シナリオを前提としています。</span><span class="sxs-lookup"><span data-stu-id="34220-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="34220-111">タスク固有のサーバー側の処理を処理するために web アプリケーションを実行する場合に、カスタム ビジネス オブジェクトを使用して**RDSServer.DataFactory**を置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="34220-111">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="34220-p103">**Query** や [CreateRecordset](query-method-rds.md) などの [RDSServer.DataFactory](createrecordset-method-rds.md) メソッドを呼び出すサーバー側ビジネス オブジェクトを作成できます。これは、ビジネス オブジェクトに機能を追加するが、既存のリモート データ サービス テクノロジも利用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="34220-p103">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="34220-114">**RDSServer.DataFactory** オブジェクトのクラス ID は、9381D8F5-0288-11D0-9501-00AA00B911A5 です。</span><span class="sxs-lookup"><span data-stu-id="34220-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

