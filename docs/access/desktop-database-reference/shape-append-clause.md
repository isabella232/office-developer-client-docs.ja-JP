---
title: Shape APPEND 句
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726352"
---
# <a name="shape-append-clause"></a>Shape APPEND 句


**適用されます**Access 2013、Office 2013。

shape コマンドの APPEND 句は、列 (1 つまたは複数) を **Recordset** に追加します。通常、この列は子 **Recordset** を参照するチャプター列です。

## <a name="syntax"></a>構文

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>説明

この句の要素を、次に示します。

- *parent-command*

- (*親コマンド*を完全に省略することがあります)、次のいずれかです。
    
  - {} オブジェクトを返すプロバイダー コマンドを波かっこ ("****") で囲んだもの。このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
  - 別の shape コマンドをかっこ ( ) で囲んだもの。
    
  - TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。

- *parent-alias*

  - 親 **Recordset** を参照する別名。省略可能です。

- *column-list*

  - 以下のいずれか 1 つまたは複数です。
    
    - 集約列。
    
    - 集計列。
    
    - NEW 句で作成された新しい列。
    
    - チャプター列。チャプター列定義は、かっこ ( ) で囲みます。次の構文を参照してください。


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- *child-recordset*

  - {} オブジェクトを返すプロバイダー コマンドを波かっこ ("****") で囲んだもの。このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
  - 別の shape コマンドをかっこ ( ) で囲んだもの。
    
  - シェイプされた既存の **Recordset** の名前。
    
  - TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。

- *child-alias*

  - 子 **Recordset** を参照する別名。

- *parent-column*

  - によって**レコード セット**内の列が返される、*親コマンドです*。

- *child-column*

  - *child-command* によって返される **Recordset** 内の列。

- *param-number*

  - 「[パラメーター化コマンドの操作](operation-of-parameterized-commands.md)」を参照してください。

- *chapter-alias*

  - 親に追加されたチャプター列を参照する別名。


> [!NOTE]
> - _「親列子の列に」_ 句は、定義されている各関係をコンマで区切って、リストでは実際には、です。
> - [!メモ] APPEND キーワードの後の句は、実際には各句をコンマで区切った一覧であり、親に追加する別の列を定義します。



## <a name="remarks"></a>解説

SHAPE コマンドの一部としてユーザー入力を使用するプロバイダー コマンドを作成すると、SHAPE はユーザーが入力したプロバイダー コマンドを内容が不明な文字列として扱い、そのままプロバイダーに渡します。たとえば、次のような SHAPE コマンドがあります。

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

図形は 2 つのコマンドを実行: 選択\*t1 からし (選択\*t2 関連の k1 に k2 から)。 場合はセミコロンで区切られた複数のプロバイダー コマンドから成る複合コマンドを指定すると、図形は、違いを識別することはありません。 それには、次の図形コマンドでは、

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

図形を選択を実行する\*から t1 です。テーブル t1 をドロップと (選択\*t2 関連の k1 に k2 から)、ドロップ テーブルは、t1 に個別に気づかずと、このケースで、危険な場合は、プロバイダー コマンドで。 アプリケーションでは、常にユーザー入力を検証して、このようなハッカーによる攻撃を防ぐ必要があります。

このセクションには、次のトピックが含まれています。

- [非パラメーター化コマンドの操作](operation-of-non-parameterized-commands.md)

- [パラメーター化コマンドの操作](operation-of-parameterized-commands.md)

- [ハイブリッド コマンド](hybrid-commands.md)

- [COMPUTE 句を使って Shape を仲介する](intervening-shape-compute-clauses.md)
