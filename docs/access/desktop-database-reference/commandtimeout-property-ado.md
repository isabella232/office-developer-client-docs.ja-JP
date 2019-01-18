---
title: CommandTimeout プロパティ (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700116"
---
# <a name="commandtimeout-property-ado"></a>CommandTimeout プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

実行しようとしたコマンドを中止して、エラーを生成するまでの待機時間を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

コマンドが実行されるまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 30 です。

## <a name="remarks"></a>解説

ネットワーク トラフィックやサーバーの過負荷により実行が遅れている **Execute** メソッドの呼び出しを取り消すことができるようにするには、 [Connection](connection-object-ado.md) オブジェクトまたは [Command](command-object-ado.md) オブジェクトの [CommandTimeout](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) プロパティを使用します。コマンドの実行が完了する前に **CommandTimeout** プロパティで設定された時間が経過すると、エラーが発生してコマンドが取り消されます。プロパティを 0 に設定すると、コマンド実行が完了するまで無限に待機します。コードを書き込むプロバイダーとデータ ソースが **CommandTimeout** 機能をサポートしていることを確認してください。

**Connection** オブジェクトの **CommandTimeout** 設定は、同じ **Connection** 上の **Command** オブジェクトの **CommandTimeout** 設定に影響しません。つまり、 **Command** オブジェクトの **CommandTimeout** プロパティは、 **Connection** オブジェクトの **CommandTimeout** の値を継承しません。

**Connection** オブジェクトでは、 **CommandTimeout** プロパティは **Connection** が開かれた後も、読み取り/書き込みが可能です。

