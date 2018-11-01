---
title: Connect プロパティ (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d9b901f925ccc009a12ef527f7bc857515042c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872404"
---
# <a name="connect-property-rds"></a>Connect プロパティ (RDS)


**適用されます**Access 2013、Office 2013。

クエリおよび更新操作が実行されるデータベース名を示します。

**Connect** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグ内で、または実行時にスクリプト コード (たとえば、VBScript) 内で設定できます。

## <a name="syntax"></a>構文

デザイン時:\<パラメーターの名前 [接続] の値を = =「接続文字列」\>

実行時間: DataControl.Connect =「接続文字列」

## <a name="parameters"></a>パラメーター

- *ConnectionString*

  - 有効な接続文字列を指定します。接続文字列全般の説明については、[ConnectionString](connectionstring-property-ado.md) プロパティかプロバイダーのマニュアルを参照してください。
    
    > [!NOTE]
    > [!メモ] **RDS.DataControl** のプロバイダーとして MS Remote を指定すると、4 層のシナリオが作成されます。3 層を超えるシナリオについては未確認なので避けてください。

- *DataControl*

  - **RDS.DataControl** オブジェクトを表すオブジェクト変数を指定します。

