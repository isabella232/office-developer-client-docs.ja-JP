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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306448"
---
# <a name="shape-append-clause"></a>Shape APPEND 句


**適用先:** Access 2013、Office 2013

shape コマンドの APPEND 句は、列 (1 つまたは複数) を **Recordset** に追加します。通常、この列は子 **Recordset** を参照するチャプター列です。

## <a name="syntax"></a>構文

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>説明

この句の要素を、次に示します。

- *parent-command*

- ゼロまたは次のいずれか (*親-コマンド*全体を省略できます)。
    
  - Recordset オブジェクトを返すプロバイダーコマンドを波{}かっこ ("") **** で囲んで指定します。 このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。 ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
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

  - Recordset オブジェクトを返すプロバイダーコマンドを波{}かっこ ("") **** で囲んで指定します。 このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。 ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
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
> - _"parent-column TO 子-column"_ 句は、実際には各リレーションシップがコンマで区切られたリストです。
> - APPEND キーワードの後の句は、実際には各句をコンマで区切った一覧であり、親に追加する別の列を定義します。



## <a name="remarks"></a>注釈

SHAPE コマンドの一部としてユーザー入力を使用するプロバイダー コマンドを作成すると、SHAPE はユーザーが入力したプロバイダー コマンドを内容が不明な文字列として扱い、そのままプロバイダーに渡します。たとえば、次のような SHAPE コマンドがあります。

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

図形は2つのコマンドを\*実行します。 t1 \*から選択します (t2 関連付け k1 から k2 へ選択します)。 ユーザーが、セミコロンで区切られた複数のプロバイダコマンドから成る複合コマンドを指定した場合、SHAPE はその違いを見分けることができません。 そのため、次の SHAPE コマンドでは、

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

図形は t1 \*から選択を実行します。drop table t1 と (t2 \*関連付け k1 から k2 へ選択します)。 drop table t1 が独立していて、この場合は危険なプロバイダコマンドであることを知らないことを示します。 アプリケーションでは、常にユーザー入力を検証して、このようなハッカーによる攻撃を防ぐ必要があります。

このセクションでは、以下のトピックについて説明します。

- [非パラメーター化コマンドの操作](operation-of-non-parameterized-commands.md)

- [パラメーター化コマンドの操作](operation-of-parameterized-commands.md)

- [ハイブリッド コマンド](hybrid-commands.md)

- [COMPUTE 句を使って Shape を仲介する](intervening-shape-compute-clauses.md)
