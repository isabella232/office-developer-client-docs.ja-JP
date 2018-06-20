---
title: PidTagDefaultViewEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802669"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>PidTagDefaultViewEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダーの既定のビューのエントリの識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|識別子:  <br/> |0x3616  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、最初のビューとして設定するフォルダー ビューのエントリの識別子です。 「標準」ビューの最初のビューとして使用する場合、プロパティを設定する必要はありません。
  
クライアント アプリケーションでは、フォルダーを開いた時にこのプロパティを取得でき、大幅なパフォーマンス向上を実現することができます。 このプロパティは、コンテンツが関連付けられているテーブルを開くと、制限を送信するのではなく、既定のビューを取得するのにはショートカットとして使用できます。
  
サービス プロバイダーの[IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)メソッドの実装は、フォルダーにコピーする際、このプロパティをコピーできます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

