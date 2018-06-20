---
title: フォーム構成ファイルの [動詞] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800097"
---
# <a name="form-configuration-file-verbs-section"></a>フォーム構成ファイルの [動詞] セクション

  
  
**適用されます**: Outlook 
  
**[動詞]** セクションには、フォームでサポートされている動詞の完全なセットが一覧表示されます。 **[動詞]** セクションの形式は次のとおりです。 
  
 **[動詞]**
  
 **Verb1** =  _の文字列_
  
**[動詞]** セクションの例を次に示します。 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

各動詞が個別に定義されている **[動詞**。 _文字列_**]** のセクションです。 A **[動詞**。 _文字列_**]** では、フォームによって提供される 1 つの動詞をについて説明します。 **表示名**のエントリを **[動詞**。 _文字列_**]** のセクションでは、ユーザー インターフェイスに表示されるコマンド名を指定します。 **コード**のエントリは、 [IMAPIForm::DoVerb](imapiform-doverb.md)メソッドに渡された動詞の数に対応します。 構文、 **[動詞**。 _文字列_**]** のセクションでは。 
  
 **[動詞です。** _文字列_**]**
  
 **表示名** =  _の文字列が表示されます_
  
 **コード** =  _の整数_
  
 **フラグ** =  _の整数_
  
 **属性にして** =  _の整数_
  
次の例では、 **[動詞**。 _文字列_**]** のセクションです。 
  
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

このセクションに記載されている動詞は、 [IMAPIFormInfo::CalcVerbSet メソッド](imapiforminfo-calcverbset.md)を使用するクライアントによって取得されます。 動詞は、フォームの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドを呼び出すと、コードの数を実行する動詞を渡すことによってアクティブ化されます。 
  

