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
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330122"
---
# <a name="pidtagresponsibility-canonical-property"></a>PidTagResponsibility 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のトランスポートプロバイダーが既にこの受信者へのメッセージの配信を承認している場合は TRUE、このトランスポートプロバイダーが責任を受け入れる必要があることを MAPI スプーラーが考慮している場合は FALSE。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESPONSIBILITY  <br/> |
|識別子:  <br/> |0x0e0f  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI ノンノンアウトテーブル  <br/> |
   
## <a name="remarks"></a>解説

mapi スプーラーがトランスポートプロバイダーに送信メッセージを送信すると、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)を介して、mapi スプーラーが責任を負うすべての受信者に対してこのプロパティが FALSE に設定され、すべてのトランスポートプロバイダーが TRUE に設定されます。その他の受信者。 トランスポートプロバイダーは、 **PR_RESPONSIBILITY**が FALSE に設定されているすべての受信者の処理を試行する必要があります。 受信者に送信または conclusively に失敗した後、トランスポートプロバイダーは、送信元のメッセージでこのプロパティを TRUE に設定して、受信者がその受信者に対して承認されたことを示す必要があります。 
  
受信者を調べた後、トランスポートプロバイダーがそれを処理できないかどうかを判断する場合は、トランスポートプロバイダーは**PR_RESPONSIBILITY**を FALSE に設定したままにします。 MAPI スプーラーは、その受信者を処理できる別のトランスポートプロバイダーを検索します。 MAPI スプーラーは、最終的に、トランスポートプロバイダーが責任を受け入れない受信者に対して、配信不能レポートを作成します。 
  
トランスポートプロバイダーがメッセージの配信を試行して失敗した場合は、mapi が配信不能レポートを生成できるように、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出してエラーの理由を mapi に示す必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序と流れを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDeleteAfterSubmit ���K���̃v���p�e�B](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

