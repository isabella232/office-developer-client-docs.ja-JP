---
title: DataFactory オブジェクト (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4090b517dfdbe6d6870c04bf4118addad861ad95
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910636"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory オブジェクト (RDSServer)


**適用されます**Access 2013、Office 2013。

この既定のサーバー側ビジネス オブジェクトは、指定されたデータ ソースの読み取り/書き込みデータ アクセス権をクライアント側アプリケーションに提供するメソッドを実装します。

## <a name="remarks"></a>備考

**RDSServer.DataFactory** オブジェクトは、クライアント要求を受け取るサーバー側 Automation オブジェクトとして設計されています。 インターネット実装では、web サーバー上に常駐し、ADISAPI コンポーネントによってインスタンス化します。 **RDSServer.DataFactory** オブジェクトは、指定されたデータ ソースの読み取り/書き込みデータ アクセス権を提供しますが、検証やビジネス ルール ロジックの機能は搭載していません。

**RDSServer.DataFactory** オブジェクトと [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの両方で使用できるメソッドを使用する場合、リモート データ サービスは既定で **RDS.DataControl** バージョンを使用します。既定では、 **RDSServer.DataFactory** が汎用のサーバー側ビジネス オブジェクトとして機能する、基本的なプログラミング シナリオを前提としています。

タスク固有のサーバー側の処理を処理するために web アプリケーションを実行する場合に、カスタム ビジネス オブジェクトを使用して**RDSServer.DataFactory**を置き換えることができます。

**Query** や [CreateRecordset](query-method-rds.md) などの [RDSServer.DataFactory](createrecordset-method-rds.md) メソッドを呼び出すサーバー側ビジネス オブジェクトを作成できます。これは、ビジネス オブジェクトに機能を追加するが、既存のリモート データ サービス テクノロジも利用する場合に便利です。

**RDSServer.DataFactory** オブジェクトのクラス ID は、9381D8F5-0288-11D0-9501-00AA00B911A5 です。

