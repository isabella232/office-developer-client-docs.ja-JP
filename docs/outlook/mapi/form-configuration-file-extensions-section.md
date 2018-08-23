---
title: フォーム構成ファイル [Extensions] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800080"
---
# <a name="form-configuration-file-extensions-section"></a>フォーム構成ファイル [Extensions] セクション

  
  
**適用対象**: Outlook 
  
**[拡張機能]** セクションには、フォーム構成ファイルの **[説明]** セクションに記載されている基本的なもの以外の任意の属性には、フォームでは、通常、名前付きプロパティを設定するの拡張属性が一覧表示されます。 拡張属性は、プロパティ タグで設定する上位ビットの**IMAPIFormInfo**オブジェクトの**GetProps**メソッドへの呼び出しから返されるプロパティです。 クライアント アプリケーションは、該当する場合、これらのタグを取得することによって、フォームの拡張属性を決定できます。 これを行うには、クライアントは、フォームのプロパティの名前を渡して、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出すし、プロパティを取得する[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
  
 **[拡張機能]**
  
 **拡張機能です。** _string1_ =  _文字列 2_
  
各拡張機能のプロパティ] セクションでは、MAPI の名前付きのプロパティの構文を使用して 1 つの拡張属性を定義します。 プロパティの型は、PT_LONG または PT_STRING8 のいずれかである必要があります。 名前付きの文字列を含むプロパティ セットはサポートされていません。 **[拡張機能]** セクションの形式は次のとおりです。 
  
 **[拡張機能です。** _文字列 2_**]**
  
 **タイプ** =  _の整数_
  
 **NmidPropset** =  _guid_
  
 **NmidInteger** =  _の整数_
  
 **値** =  _文字列_ |  _の整数_
  
次の **[拡張機能]** セクションおよびそれ以降の関連するセクションの例が表示されます。 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


