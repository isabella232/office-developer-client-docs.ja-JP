---
title: Shape APPEND 句
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c0304e104953a5c95f25ca22ba719756dccc6ecc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605919"
---
# <a name="shape-append-clause"></a>Shape APPEND 句


**適用先**: Access 2013、Office 2013

shape コマンドの APPEND 句は、列 (1 つまたは複数) を **Recordset** に追加します。通常、この列は子 **Recordset** を参照するチャプター列です。

## <a name="syntax"></a>構文

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>説明

この句の要素を、次に示します。

- *parent-command*

- 0 または次のいずれかを指定します (親コマンドは *完全に* 省略できます)。
    
  - Recordset オブジェクトを返す中かっこ (" {} ") 内の **プロバイダー コマンド** 。 このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。 ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
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

  - Recordset オブジェクトを返す中かっこ (" {} ") 内の **プロバイダー コマンド** 。 このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。 ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
  - 別の shape コマンドをかっこ ( ) で囲んだもの。
    
  - シェイプされた既存の **Recordset** の名前。
    
  - TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。

- *child-alias*

  - 子 **Recordset** を参照する別名。

- *parent-column*

  - *parent-command* によって返される **Recordset** 内の列。

- *child-column*

  - *child-command* によって返される **Recordset** 内の列。

- *param-number*

  - 「[パラメーター化コマンドの操作](operation-of-parameterized-commands.md)」を参照してください。

- *chapter-alias*

  - 親に追加されたチャプター列を参照する別名。


> [!NOTE]
> - _"parent-column TO child-column"_ 句は実際にはリストで、定義された各関係はコンマで区切られます。
> - APPEND キーワードの後の句は、実際には各句をコンマで区切った一覧であり、親に追加する別の列を定義します。



## <a name="remarks"></a>注釈

SHAPE コマンドの一部としてユーザー入力を使用するプロバイダー コマンドを作成すると、SHAPE はユーザーが入力したプロバイダー コマンドを内容が不明な文字列として扱い、そのままプロバイダーに渡します。たとえば、次のような SHAPE コマンドがあります。

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE では、t1 から選択し \* \* 、t2 RELATE k1 TO k2 から選択する 2 つのコマンドを実行します。 ユーザーがセミコロンで区切られた複数のプロバイダー コマンドで構成される複合コマンドを指定した場合、SHAPE は違いを識別できます。 したがって、次の SHAPE コマンドでは、

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE は t1 から選択を実行し、ドロップ テーブル t1 と \* (t2 RELATE k1 TO k2 から選択) を実行します。ドロップ テーブル t1 が別個であり、この場合、危険なプロバイダー コマンドである場合は実現されません。 \* アプリケーションでは、常にユーザー入力を検証して、このようなハッカーによる攻撃を防ぐ必要があります。

このセクションでは、以下のトピックについて説明します。

- [非パラメーター化コマンドの操作](operation-of-non-parameterized-commands.md)

- [パラメーター化コマンドの操作](operation-of-parameterized-commands.md)

- [ハイブリッド コマンド](hybrid-commands.md)

- [COMPUTE 句を使って Shape を仲介する](intervening-shape-compute-clauses.md)
