---
title: PidTagAttachRendering 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361097"
---
# <a name="pidtagattachrendering-canonical-property"></a>PidTagAttachRendering 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのレンダリング情報を含む Microsoft Windows メタファイルが保存されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_RENDERING  <br/> |
|識別子:  <br/> |0x3709  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの目的は、添付ファイルの時点で親メッセージ内に表示できるアイコンまたはその他の画像表現を提供することです。 このような表現には、通常、添付ファイルの名前、添付ファイルの種類 (Microsoft Office Word 文書など) が含まれます。 クライアントアプリケーションは、メッセージの表示でこの表現を使用できます。 
  
添付ファイルの場合、このプロパティは通常、ファイルのアイコンを portrays ます。 
  
添付されたメッセージの場合、このプロパティは通常設定されません。 添付されたメッセージをレンダリングする必要のあるクライアントアプリケーションは、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得し、対応するフォーム情報オブジェクトへのポインターに対して[imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出します。そのオブジェクトで[imapiforminfo](imapiforminfoimapiprop.md)インターフェイスを開き、 **GetProps**を使用して**PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) または**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティを取得します。 
  
埋め込み静的な OLE オブジェクトの場合、このプロパティには、ウィンドウに添付ファイルの表示を描画するために使用できる Microsoft Windows メタファイルが含まれています。 
  
埋め込まれた動的 OLE オブジェクトの場合、クライアントは ole データを使用してレンダリング情報を生成する必要があります。 
  
すべての場合において、クライアントアプリケーションは、このプロパティが通常数百バイトで、添付ファイルテーブルで切り捨てられる可能性があることを認識しておく必要があります。 クライアントが添付ファイル自体を開かずに、このプロパティから添付ファイルをレンダリングする場合は、テーブルの切り捨てルール内で作業する必要があります。 詳細については、「[大きな列の作業](working-with-large-columns.md)」を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
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

