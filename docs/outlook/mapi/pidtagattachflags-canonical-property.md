---
title: PidTagAttachFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b934f9694061e17118be35e3fabeeff3bbc61a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802467"
---
# <a name="pidtagattachflags-canonical-property"></a>PidTagAttachFlags の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルのフラグのビットマスクを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_FLAGS  <br/> |
|識別子:  <br/> |0x3714  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが使用される MHTML をサポートするためです。 
  
**PR_ATTACH_FLAGS**ビットマスクについては、次のフラグの 1 つ以上を設定できます。 
  
ATT_INVISIBLE_IN_HTML 
  
> この添付ファイルが HTML のレンダリング アプリケーションで使用可能ではありませんし、多目的インターネット メール拡張機能 (MIME) の処理で無視するかを示します。 
    
ATT_INVISIBLE_IN_RTF 
  
> この添付ファイルをリッチ テキスト形式 (RTF) でのレンダリング アプリケーションで使用可能ではありませんし、MAPI によって無視されることを示します。
    
**PR_ATTACH_FLAGS**プロパティが 0 の場合または省略すると、添付ファイルでは、すべてのアプリケーションによって処理されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

