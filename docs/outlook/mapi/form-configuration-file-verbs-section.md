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
  
**[verb]** セクションには、フォームでサポートされている動詞の完全なセットが表示されます。 **[verb]** セクションの形式は次のとおりです。 
  
 **動詞**
  
 **Verb1** =  _文字列_
  
**[verb]** セクションの例を次に示します。 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

各動詞は個別の [動詞で定義されて**います。** _文字列_**]** セクション A **[動詞。** _文字列_**]** セクションでは、フォームで提供される1つの動詞について説明します。 **[動詞**内の**DisplayName**エントリ。 _文字列_**]** セクションは、ユーザーインターフェイスに表示されるコマンド名を指定します。 **コード**エントリは、imapiform で渡された動詞番号に対応します[::D overb](imapiform-doverb.md)メソッド。 [動詞の構文を使用し**ます。** _文字列_**]** セクションは次のとおりです。 
  
 **xexch50.** _文字列_**]**
  
 **DisplayName** =  _表示文字列_
  
 **コード** =  _整数_
  
 **Flags** =  _整数_
  
 **Attribs** =  _整数_
  
次に、[動詞の例を示し**ます。** _文字列_**]** セクション 
  
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

このセクションに記載されている動詞は、 [imapiforminfo:: CalcVerbSet メソッド](imapiforminfo-calcverbset.md)を使用してクライアントによって取得されます。 動詞は、フォームの[imapiform::D overb](imapiform-doverb.md)メソッドを呼び出し、実行する動詞のコード番号を渡すことによってアクティブ化されます。 
  

