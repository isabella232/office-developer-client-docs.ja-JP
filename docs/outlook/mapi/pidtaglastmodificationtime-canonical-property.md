---
title: PidTagLastModificationTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bf58e0598af6eb833b003b824be95f8fb82bd8bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19802939"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>PidTagLastModificationTime の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
日付と時刻のオブジェクトまたはサブオブジェクトの最終変更日時が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|識別子:  <br/> |0x3008  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |メッセージの時刻  <br/> |
   
## <a name="remarks"></a>Remarks

**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) のプロパティと同じ値には、このプロパティは設定が最初にします。 添付ファイルの下位オブジェクトを更新できます、必要に応じて、ネイティブ ファイル システムによって保持される最後の変更時刻をコピーすることによって。 クライアント アプリケーションは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの最初の呼び出しまで、このプロパティを設定できます。 プロバイダーは、すべての**IMAPIProp::SaveChanges**の呼び出し中に**PR_LAST_MODIFICATION_TIME**を更新する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
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

