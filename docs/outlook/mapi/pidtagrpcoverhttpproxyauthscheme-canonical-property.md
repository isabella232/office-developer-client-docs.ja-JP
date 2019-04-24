---
title: PidTagRpcOverHttpProxyAuthScheme 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ea4b90bf1190fd71701f82d43aaee384c7987ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331312"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a>PidTagRpcOverHttpProxyAuthScheme 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このプロファイルに使用される認証プロトコルを表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROH_PROXY_AUTH_SCHEME  <br/> |
|識別子:  <br/> |0x6627  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、基本認証または NT LAN Manager (NTLM) 認証のいずれかに設定できます。 このプロパティに指定できる値は、次のとおりです。
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**ROHAUTH_BASIC** <br/> |0x1  <br/> |基本認証  <br/> |
|**ROHAUTH_NTLM** <br/> |0x2  <br/> |NTLM 認証  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

