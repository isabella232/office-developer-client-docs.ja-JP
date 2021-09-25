---
title: Relation.PartialReplica プロパティ (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c674003234bb4b5e961651e85b87342ad49486e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564933"
---
# <a name="relationpartialreplica-property-dao"></a>Relation.PartialReplica プロパティ (DAO)

**適用先:** Access 2013、Office 2013

フル レプリカから部分レプリカに値を設定するときに、 **Relation** オブジェクトのリレーションシップを考慮する必要があるかどうかを示す値を設定または取得します (Microsoft Access データベース エンジンのデータベースのみ)。値の取得および設定が可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式* .PartialReplica

*式* Relation オブジェクトを返 **す式** 。

## <a name="remarks"></a>注釈

設定値または戻り値はブール型 (Boolean) の値で、同期時にこのリレーションシップを適用する必要がある場合は **True** です。

このプロパティを使用すると、テーブル間のリレーションシップに基づいて、フル レプリカのデータを部分レプリカにレプリケートできます。**ReplicaFilter** プロパティの設定のみでは部分レプリカにレプリケートする必要のあるデータを適切に指定できない場合に、**PartialReplica** プロパティを使用できます。たとえば、顧客テーブルが注文テーブルと一対多のリレーションシップを持つデータベースがあり、すべての注文ではなくカリフォルニア地域の顧客からの注文のみをレプリケートする部分レプリカを構成するとします。Region フィールドは注文テーブルではなく顧客テーブルにあるため、注文テーブルの **ReplicaFilter** プロパティを Region = 'CA' に設定することはできません。

カリフォルニア地域からのすべての注文をレプリケートするには、レプリケーション時に注文テーブルと顧客テーブル間のリレーションシップがアクティブになるように指定する必要があります。部分レプリカを作成した後、以下の手順を実行すると、カリフォルニア地域からのすべての注文が部分レプリカに設定されます。

1.  Customers **TableDef オブジェクト** の **ReplicaFilter** プロパティを "Region = 'CA' に設定します。

2.  注文テーブルと顧客テーブル間のリレーションシップに対応する **Relation** オブジェクトの **PartialReplica** プロパティの値を **True** に設定します。

3.  **PopulatePartial** メソッドを呼び出します。
    

> [!NOTE]
> [!メモ] レプリカ フィルターまたはレプリカ リレーションシップを設定した場合、部分レプリカ内の制限条件を満たさないレコードは部分レプリカから削除されますが、フル レプリカからは削除されません。 たとえば、部分レプリカの顧客 **TableDef** オブジェクトの **ReplicaFilter** プロパティを "Region = 'CA'" に設定し、データベースにもう一度値を設定するとします。 これにより、カリフォルニア地域の顧客のすべてのレコードが挿入または更新されます。 
> 
> 次に、**ReplicaFilter** プロパティを "Region = 'FL'" に再設定し、データベースにもう一度値を設定すると、部分レプリカ内にあるカリフォルニア地域のすべてのレコードが削除され、フル レプリカからフロリダ地域の顧客のすべてのレコードが挿入されます。 フル レプリカ内のレコードは削除されません。 
>
> **ReplicaFilter** プロパティまたは **PartialReplica** プロパティを設定する前に、これらのプロパティを設定する部分レプリカをフル レプリカと同期させることをお勧めします。 これにより、部分レプリカ内のすべてのレコードが削除される前に、部分レプリカの保留中の変更がフル レプリカに反映されます。


