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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719338"
---
# <a name="running-business-objects-in-component-services"></a>コンポーネント サービスでのビジネス オブジェクトの実行

**適用されます**Access 2013、Office 2013。

ビジネス オブジェクトには、実行可能ファイル (.exe) とダイナミック リンク ライブラリ (.dll) があります。ビジネス オブジェクトを実行するために使う構成は、そのオブジェクトが .dll ファイルであるか .exe ファイルであるかによって異なります。

- .exe ファイルとして作成されたビジネス オブジェクトは、DCOM を介して呼び出すことができます。これらのビジネス オブジェクトがインターネット インフォメーション サービス (IIS) を介して使用される場合は、データの追加マーシャリングの対象となるため、クライアントのパフォーマンスが低下します。

- .dll ファイルとして作成されたビジネス オブジェクトは、IIS (したがって HTTP) を介して利用できます。また、コンポーネント サービス (Windows NT を使用している場合は Microsoft Transaction Server) を介する場合のみ、DCOM からも利用できます。IIS を介してアクセスできるようにするには、IIS サーバー コンピューターにビジネス オブジェクト DLL を登録する必要があります。DCOM で DLL を実行するための構成方法の手順については、「[DCOM で DLL を実行できるようにする](enabling-a-dll-to-run-on-dcom.md)」を参照してください。


> [!NOTE]
> 中間層のビジネス オブジェクトは、コンポーネント サービスのコンポーネント ( **GetObjectContext**、 **SetComplete**、および**SetAbort**を使用) として実装されているを使って、コンポーネント サービス (または Windows NT を使用している場合は MTS) コンテキスト オブジェクトを複数のクライアント呼び出し間で状態を維持します。 このシナリオは、通常は信頼関係のあるクライアントとサーバー (イントラネット) 間で実装される DCOM でも可能です。 
>
> その場合、クライアント側の [RDS.DataSpace](dataspace-object-rds.md) オブジェクトと [CreateObject](createobject-method-rds.md) メソッドはトランザクション コンテキスト オブジェクトと **CreateInstance** メソッド ( **ITransactionContext** インターフェイスによって提供) に置き換えられ、コンポーネント サービスによって実装されます。


## <a name="see-also"></a>関連項目

- [コンポーネント サービス (SQL Server) のビジネス オブジェクトを実行しています。](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
