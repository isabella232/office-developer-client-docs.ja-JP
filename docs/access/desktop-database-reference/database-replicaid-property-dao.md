---
title: Database.ReplicaID プロパティ (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3214f093b90576483df4d6f63cf1ad62b3530931
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918766"
---
# <a name="databasereplicaid-property-dao"></a>Database.ReplicaID プロパティ (DAO)


**適用されます**Access 2013、Office 2013。


データベース レプリカを一意に識別する 16 バイトの値を取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。ReplicaID

*式***データベース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

戻り値は、レプリカまたはデザイン マスターを一意に識別する GUID 型 ( **GUID**) の値です。

Microsoft Access データベース エンジンは、新規レプリカの作成時にこの値を自動的に生成します。

各レプリカ (およびデザイン マスター) の **ReplicaID** プロパティは、MSysReplicas システム テーブルに保存されます。

## <a name="example"></a>例

この例では、Northwind.mdb のデザイン マスターからレプリカを作成し、Microsoft Access データベース エンジンによって自動的に作成されるレプリカの **ReplicaID** を返します (Northwind のデザイン マスターをまだ作成していない場合は、 **Replicable** プロパティを参照するか、コード内のデータベース名を既存のデザイン マスターに変更します)。

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

