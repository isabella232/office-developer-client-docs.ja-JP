---
title: PidTagAttachRendering 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0571d7726c17334867138346f92e99deccf9f259
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600457"
---
# <a name="pidtagattachrendering-canonical-property"></a>PidTagAttachRendering 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのレンダリングWindowsを含む Microsoft のメタファイルを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_RENDERING  <br/> |
|識別子:  <br/> |0x3709  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの目的は、添付ファイルの時点で親メッセージ内に表示できるアイコンまたは他の図の表現を提供します。 このような表現には、通常、添付ファイルの名前 (もし含まれる場合) と、添付ファイルの性質 (Word 文書などのMicrosoft Officeが含まれます。 クライアント アプリケーションは、メッセージの表示でこの表現を使用できます。 
  
添付ファイルの場合、このプロパティは通常、ファイルのアイコンを表示します。 
  
添付メッセージの場合、通常、このプロパティは設定されません。 添付メッセージをレンダリングする必要があるクライアント アプリケーションは、その **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得し、対応するフォーム情報オブジェクトへのポインターに対して [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出し、そのオブジェクトの [IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスを開き **、GetProps** を使用して **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティまたは PR_MINI_ICON ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティを取得する必要があります。  
  
埋め込み静的 OLE オブジェクトの場合、このプロパティには、ウィンドウに添付ファイルWindows描画するために使用できる Microsoft のメタファイルが含まれる。 
  
埋め込み動的 OLE オブジェクトの場合、クライアントは OLE データを使用してレンダリング情報を生成する必要があります。 
  
すべての場合、クライアント アプリケーションは、このプロパティのサイズは通常数百バイトであり、添付ファイル テーブルの切り捨ての対象となります。 クライアントが添付ファイル自体を開かなくてもこのプロパティから添付ファイルをレンダリングする場合は、テーブルの切り捨てルール内で動作する必要があります。 詳細については、「大規模な列の [操作」を参照してください](working-with-large-columns.md)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

