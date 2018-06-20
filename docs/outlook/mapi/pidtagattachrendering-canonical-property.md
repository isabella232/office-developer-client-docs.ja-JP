---
title: PidTagAttachRendering の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802493"
---
# <a name="pidtagattachrendering-canonical-property"></a>PidTagAttachRendering の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルの表示情報を使用して Microsoft Windows メタファイルが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_RENDERING  <br/> |
|識別子:  <br/> |0x3709  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの目的は、アイコン、またはその他の添付ファイルの時点で親のメッセージ内で表示可能な図で表現を提供することにします。 通常、このような表現には、存在する場合、添付ファイルの名前や、Microsoft Office Word 文書の添付ファイルの内容が含まれます。 クライアント アプリケーションは、メッセージの表示で、この表現を使用できます。 
  
添付ファイルの場合、このプロパティは通常、ファイルのアイコンを示します。 
  
添付されているメッセージでは、このプロパティは、通常設定されません。 添付メッセージをレンダリングする必要があるクライアント アプリケーションは、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを取得する必要があります、 [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を対応するフォームについては、オブジェクトへのポインターの呼び出し、そのオブジェクトの[IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスを開き、 **GetProps**を使用して、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) または**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティを取得します。 
  
埋め込み静的 OLE オブジェクトは、このプロパティには、ウィンドウで、添付ファイルの形式を描画に使用できる Microsoft Windows メタファイルが含まれています。 
  
動的埋め込み OLE オブジェクトをクライアントは、レンダリング情報を生成するのに OLE データを使用する必要があります。 
  
すべての場合、クライアント アプリケーションはこのプロパティがいくつかの数百バイトのサイズは、通常、添付ファイル テーブルの切り捨ての対象となることに注意することはあります。 クライアント自体の添付ファイルを開かずにこのプロパティから添付ファイルをレンダリングする場合は、テーブルの切り捨てルール内で作業する必要があります。 詳細については、[大規模な列の使用](working-with-large-columns.md)を参照してください。 
  
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

