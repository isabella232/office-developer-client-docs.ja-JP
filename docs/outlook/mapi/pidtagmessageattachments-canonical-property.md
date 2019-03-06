---
title: PidTagMessageAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413974"
---
# <a name="pidtagmessageattachments-canonical-property"></a>PidTagMessageAttachments 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイルの表が保存されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|識別子:  <br/> |0x0e13  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>Remarks

このプロパティは、 [imapiprop:: CopyTo](imapiprop-copyto.md)操作で除外することも、 [imapiprop:: copyprops](imapiprop-copyprops.md)操作に含めることもできます。 PT_OBJECT 型のプロパティとして、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドによって正常に取得することはできません。 このコンテンツは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドによってアクセスされ、 **IID_IMAPITable**インターフェイスの識別子が要求されます。 サービスプロバイダーは、設定されている場合は[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドに報告する必要がありますが、設定されていない場合はレポートすることができます。 
  
表の内容を取得するには、クライアントアプリケーションは[IMessage:: getattachmenttable](imessage-getattachmenttable.md)メソッドを呼び出す必要があります。 �ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B 
  
このプロパティは、 [ssubrestriction](ssubrestriction.md)構造で指定することによって、サブプロパティの制限に使用できます。 これにより、クライアントは、指定した条件に一致する添付ファイルを持つメッセージにコンテナーのビューを制限できます。 添付ファイルテーブルにある1つ以上の行、つまり1つの添付ファイルがサブオブジェクト制限を満たす場合は、メッセージが表示されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。
    
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

