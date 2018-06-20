---
title: PidTagAttachPayloadProviderGuidString の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9e581f040b3d7d9e204dd41431b1eba650b971a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802494"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>PidTagAttachPayloadProviderGuidString の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
MIME X ・ ペイロード ・ プロバイダーの Guid のヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR、PR_ATTACH_PAYLOAD_PROV_GUID_STR_A、PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|識別子:  <br/> |0x3719  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティの値を設定するのには MIME クライアントは、添付ファイルとして解析される MIME エンティティに X のペイロード ・ プロバイダーの Guid のヘッダー フィールドを記述する必要があります。
  
MIME のリーダーでは、このヘッダー フィールドの値を対応するプロパティの値にコピーする必要があります。 MIME のリーダーは、添付ファイルとしてではなく、メッセージまたはメッセージの本文として分析する MIME エンティティ上に表示されるとき、このヘッダー フィールドを無視してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
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

