---
title: PidTagResponsibility 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2a1c49b29ba08775768fc74861ba36b3c6356fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589379"
---
# <a name="pidtagresponsibility-canonical-property"></a>PidTagResponsibility 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI スプーラーは、このトランスポート プロバイダーが責任を受け入れる必要がありますと見なされる場合は、この受信者、および FALSE にメッセージを配信する責任をいくつかのトランスポート プロバイダーが既に受け入れられて場合は、TRUE を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |れない  <br/> |
|識別子:  <br/> |0x0E0F  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

FALSE にこのプロパティを設定する MAPI スプーラーを無効と見なされるトランスポート プロバイダー責任、および TRUE すべての受信者のすべての MAPI スプーラーが[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)、によって、トランスポート プロバイダーに送信メッセージを表示するとき他の受信者です。 トランスポート プロバイダーは必要があります**れない**が FALSE に設定を持つすべての受信者を処理しようとしています。 正常に送信する、または受信者への送信に失敗して確定した後トランスポート プロバイダーは、送信元のメッセージ受信者の責任を受け入れたことを示すには TRUE にこのプロパティを設定する必要があります。 
  
受信者を調べると後、は、トランスポート プロバイダーは、できないこと、または処理する必要があります決定したら場合、トランスポート プロバイダーは、必要があります [**れない**に false を指定します。 MAPI スプーラーは、その受信者を処理できる別のトランスポート プロバイダーを探します。 MAPI スプーラーは、最終的には対象のトランスポート プロバイダーを負いません責任のいずれかの受信者に配信不能レポートを作成します。 
  
トランスポート プロバイダーは、しようと、メッセージの配信に失敗した場合、MAPI は、配信不能レポートを生成できるように、MAPI への障害の理由を示すために[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出す必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDeleteAfterSubmit ���K���̃v���p�e�B](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

