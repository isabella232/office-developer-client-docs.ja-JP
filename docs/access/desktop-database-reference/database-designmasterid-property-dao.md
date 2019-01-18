---
title: Database.DesignMasterID プロパティ (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a189d16880fccdc34c169aee61c6781e1d86afa8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703910"
---
# <a name="databasedesignmasterid-property-dao"></a>Database.DesignMasterID プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

レプリカ セットでデザイン マスターを一意に識別する 16 バイトの値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。DesignMasterID

*式***データベース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**DesignMasterID** プロパティを設定するのは、現在のデザイン マスターを移動する必要がある場合のみです。このプロパティを設定すると、レプリカ セットの特定のレプリカがデザイン マスターになります。

> [!NOTE]
> [!メモ] レプリカ セットで 2 つ目のデザイン マスターを作成しないでください。2 つ目のデザイン マスターが存在すると、データが失われる可能性があります。

デザイン マスターの削除や破損などの特殊な状況下では、現在のレプリカでこのプロパティを設定できます。ただし、レプリカ セットに既に別のデザイン マスターが存在するときに、レプリカでこのプロパティを設定すると、レプリカ セットが 2 つの調整不可能なセットに分割され、それ以降のデータの同期が行われなくなる可能性があります。

レプリカをセットの新しいデザイン マスターにする場合は、レプリカ セットのすべてのレプリカと同期してから、レプリカの **DesignMasterID** プロパティを設定します。レプリカをデザイン マスターにするには、レプリカを排他モードで開く必要があります。

読み取り専用として指定されているレプリカをデザイン マスターにすると、対象のレプリカは読み取り/書き込みが可能になり、古いデザイン マスターも引き続き読み取り/書き込みが可能です。

**DesignMasterID** プロパティの設定値は、MSysRepInfo システム テーブルに保存されます。

## <a name="example"></a>例

次の使用例は、 **DesignMasterID** プロパティを別のデータベースの **ReplicaID** プロパティの設定値に設定し、そのデータベースをレプリカ セットのデザイン マスターにします。新旧のデザイン マスターが同期されて、デザインの変更が更新されます。このコードが機能するには、デザイン マスターとレプリカを作成し、必要に応じてその名前とパスを含め、このコードを新旧のデザイン マスター以外のデータベースから実行する必要があります。

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

