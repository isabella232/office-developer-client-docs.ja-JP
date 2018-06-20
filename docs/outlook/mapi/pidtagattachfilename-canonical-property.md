---
title: PidTagAttachFilename の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4468ecd5946c95fab62d0885d9c0b3343a1508dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802477"
---
# <a name="pidtagattachfilename-canonical-property"></a>PidTagAttachFilename の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルのベース ファイル名とパスを除外する拡張子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_FILENAME、PR_ATTACH_FILENAME_A、PR_ATTACH_FILENAME_W  <br/> |
|識別子:  <br/> |0x3704  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

オブジェクトの添付ファイルが**PR_ATTACH_METHOD**の**ATTACH_BY_VALUE**、 **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、および**ATTACH_BY_REF_ONLY**の値に関係するこれらのプロパティを公開することをお勧めします。([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) のプロパティです。 **PR_ATTACH_FILENAME**と関連付けられているプロパティは、必要な場合これらの値のいずれかを使用します。 
  
**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) のプロパティが指定されていない場合は、ファイル名の拡張子を指定して、添付ファイルを保存するため、これらのプロパティを既定のファイル名として使用できます。 
  
ファイル名は、8 文字および 3 文字の拡張子に制限されます。 長いファイル名をサポートしているプラットフォームでは、このプロパティと**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) のプロパティの両方を設定します。 
  
MAPI の機能をファイル名に、および米国規格協会 (ANSI) 文字セットで、その他の文字列が渡されます。 正規機器製造元 (OEM) 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
[[MS OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> S/MIME 署名され、暗号化メッセージのプロパティを指定します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
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

