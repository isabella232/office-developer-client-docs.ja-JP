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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330122"
---
# <a name="pidtagresponsibility-canonical-property"></a>PidTagResponsibility 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のトランスポート プロバイダーがメッセージをこの受信者に配信する責任を既に受け入れた場合は TRUE、MAPI スプーラーがこのトランスポート プロバイダーが責任を受け入れる必要があると考える場合は FALSE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESPONSIBILITY  <br/> |
|識別子:  <br/> |0x0E0F  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

MAPI スプーラーが [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を介してトランスポート プロバイダーに送信メッセージを表示すると、MAPI スプーラーがトランスポート プロバイダーを担当すると見なすすべての受信者に対してこのプロパティを FALSE に設定し、他のすべての受信者に対して TRUE を設定します。 トランスポート プロバイダーは、FALSE に設定されている受信者 **をPR_RESPONSIBILITYする** 必要があります。 受信者への送信に成功した、または決定的に失敗した後、トランスポート プロバイダーは、ソース メッセージでこのプロパティを TRUE に設定して、その受信者に対する責任を受け入れるかどうかを示す必要があります。 
  
受信者を調べた後で、トランスポート プロバイダーが受信者を処理できないか処理しないかを判断した場合、トランスポート プロバイダーは false に設定 **PR_RESPONSIBILITYする必要** があります。 MAPI スプーラーは、その受信者を処理できる別のトランスポート プロバイダーを探します。 MAPI スプーラーは最終的に、トランスポート プロバイダーが責任を受け入れる受信者に対して配信不可のレポートを作成します。 
  
トランスポート プロバイダーがメッセージの配信を試み、失敗した場合は、MAPI にエラーの理由を示す [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを呼び出して、MAPI が配信不能レポートを生成できるようにする必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagDeleteAfterSubmit ���K���̃v���p�e�B](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

