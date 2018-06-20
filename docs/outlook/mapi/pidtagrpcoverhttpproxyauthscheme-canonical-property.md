---
title: PidTagRpcOverHttpProxyAuthScheme の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b8c68c2cd34ba037dc725a7d15575159466d8123
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803364"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a>PidTagRpcOverHttpProxyAuthScheme の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このプロファイルに使用する認証プロトコルを表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ROH_PROXY_AUTH_SCHEME  <br/> |
|識別子:  <br/> |0x6627  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、基本認証または NT LAN マネージャー (NTLM) 認証のいずれかを設定できます。 このプロパティの有効な値は、次のような。
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**ROHAUTH_BASIC** <br/> |0x1  <br/> |基本認証  <br/> |
|**ROHAUTH_NTLM** <br/> |0x2  <br/> |NTLM 認証  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

