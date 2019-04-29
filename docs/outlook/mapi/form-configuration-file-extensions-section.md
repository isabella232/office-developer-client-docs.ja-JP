---
title: フォーム構成ファイル [Extensions] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423756"
---
# <a name="form-configuration-file-extensions-section"></a>フォーム構成ファイル [Extensions] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[Extensions]** セクションには、フォームの拡張属性 (通常は名前付きプロパティセット) が一覧表示されます。これは、フォーム構成ファイルの **[Description]** セクションに示されている基本の属性以外の属性でもあります。 拡張属性は、プロパティタグで high bit が設定された**imapiforminfo**オブジェクトの**GetProps**メソッドへの呼び出しから返されるプロパティです。 クライアントアプリケーションは、これらのタグを取得することによって、フォームの拡張属性を決定できます。 そのためには、クライアントは[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出し、フォームのプロパティの名前を渡し、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出してプロパティを取得します。 
  
 **Extensions**
  
 **Extension.** _string1_ =  文字列 (_string2_ )
  
各拡張プロパティセクションは、MAPI 名前付きプロパティの構文を使用して、1つの拡張属性を定義します。 プロパティの種類は、PT_LONG または PT_STRING8 のいずれかである必要があります。 名前付き文字列を含むプロパティセットはサポートされていません。 **[Extension]** セクションの形式は次のとおりです。 
  
 **Extension.** _string2_**]**
  
 **** =  _整数_型
  
 **NmidPropset** =  _guid_
  
 **nmidinteger** =  _整数_
  
 **値** =  __ 文字列 |  _整数_
  
**[Extensions]** セクションの例と、それに続く関連セクションを次に示します。 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


