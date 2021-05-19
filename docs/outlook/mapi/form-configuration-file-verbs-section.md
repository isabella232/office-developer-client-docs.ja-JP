---
title: フォーム構成ファイル [Verbs] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417785"
---
# <a name="form-configuration-file-verbs-section"></a>フォーム構成ファイル [Verbs] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[Verbs] セクションには**、フォームでサポートされている動詞の完全なセットが一覧表示されます。 **[Verbs] セクションの形式は** 次の形式です。 
  
 **[Verbs]**
  
 **Verb1**  =  _string_
  
[Verbs] セクションの **例を次に示** します。 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

各動詞は、個別の **[Verb] で定義されます。** _string_ **]** セクション。 A **[Verb.** _string_ **] セクション** では、フォームによって提供される単一の動詞について説明します。 **[Verb]** の **DisplayName エントリ。** _string_ **] セクション** は、ユーザー インターフェイスに表示されるコマンド名を指定します。 Code **エントリ** は [、IMAPIForm::D oVerb メソッドで渡される動詞番号に対応](imapiform-doverb.md) します。 [Verb] **の構文を指定します。** _string_ **] セクション** は次の場合です。 
  
 **[動詞]** _string_ **]**
  
 **DisplayName**  =  _表示される文字列_
  
 **コード**  =  _integer_
  
 **フラグ**  =  _integer_
  
 **Attribs**  =  _integer_
  
[Verb] の例を **次に示します。** _string_ **]** セクション。 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

このセクションに記載されている動詞は [、IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドを使用してクライアントによって取得されます。 動詞は、フォームの [IMAPIForm::D oVerb](imapiform-doverb.md) メソッドを呼び出し、実行する動詞のコード番号を渡すことによってアクティブ化されます。 
  

