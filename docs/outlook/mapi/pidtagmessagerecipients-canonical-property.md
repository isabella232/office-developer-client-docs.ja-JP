---
title: PidTagMessageRecipients 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3de07cb20d760a335f90ecacbea3bcc8b0a39512
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619954"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>PidTagMessageRecipients 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限を満たす受信者サブオブジェクトを含むすべてのメッセージを検索するためにコンテンツ テーブルに適用できる制限のテーブルが含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|識別子:  <br/> |0x0E12  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。 型の **プロパティPT_OBJECT** [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドでは正常に取得できません。 その内容にアクセスするには [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを使用して、インターフェイス識別子 **IID_IMAPITableする必要** があります。 サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合は、必要に応じて報告する場合があります。 
  
表の内容を取得するには、クライアント アプリケーションが [IMessage::GetRecipientTable メソッドを呼び出す必要](imessage-getrecipienttable.md) があります。 
  
このプロパティは [、SSubRestriction](ssubrestriction.md) 構造で指定することで、サブオブジェクト制限に使用できます。 これにより、クライアントはコンテナーのビューを、指定された条件を満たす受信者とのメッセージに制限できます。 メッセージは、受信者テーブル内の少なくとも 1 行(つまり、1 人の受信者がサブオブジェクト制限を満たす場合)を表示する資格を与える。 
  
 **メモ** サブオブジェクト制限の結果の使用は、テーブル内のすべてのメッセージに対する [IMAPISession::OpenEntry](imapisession-openentry.md) 呼び出しと同じです。 クライアント アプリケーションと検索するメッセージの数に応じて、パフォーマンスに影響を与える可能性があります。 
  
プロパティ **PR_MESSAGE_ATTACHMENTS** プロパティ [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)プロパティと、このプロパティは使用法で似ています。 複数の MAPI プロパティを使用すると、テーブルにアクセスできます。 
  
|**プロパティ**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |コンテンツ テーブル  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |階層テーブル  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |関連付けられたコンテンツ テーブル  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |添付ファイルテーブル  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |受信者テーブル  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
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

