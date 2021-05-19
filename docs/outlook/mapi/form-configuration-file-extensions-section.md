---
title: フォーム構成ファイル [拡張機能] セクション
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
# <a name="form-configuration-file-extensions-section"></a>フォーム構成ファイル [拡張機能] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[Extensions]** セクションには、フォームの拡張属性 (通常は名前付きプロパティ セット) が一覧表示されます。これは、フォーム構成ファイルの **[Description]** セクションに記載されている基本的な属性を超える属性です。 拡張属性は、プロパティ タグにハイ ビットが設定された **IMAPIFormInfo** オブジェクトの **GetProps** メソッドの呼び出しから返されるプロパティです。 クライアント アプリケーションは、これらのタグを取得することで、フォームの拡張属性がある場合は、その属性を特定できます。 これを行うには、クライアントは [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを呼び出し、フォームのプロパティの名前を渡し [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出してプロパティを取得します。 
  
 **[拡張機能]**
  
 **拡張機能。** _string1_  =  _string2_
  
各拡張プロパティ セクションでは、MAPI 名前付きプロパティ構文を使用して 1 つの拡張属性を定義します。 プロパティの種類は、プロパティの種類PT_LONGまたはPT_STRING8。 名前付き文字列を含むプロパティ セットはサポートされていません。 [拡張] **セクションの形式は** 次の形式です。 
  
 **[拡張機能]** _string2_ **]**
  
 **型**  =  _integer_
  
 **NmidPropset**  =  _guid_
  
 **NmidInteger**  =  _integer_
  
 **値**  =  _string_  |  _integer_
  
**[Extensions] セクションとそれに** 続く関連セクションの例を次に示します。 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


