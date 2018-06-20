---
title: PidLidRemoteTransport の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802147"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
どのようなアカウントのヘッダー項目に関連付けられて、POP を置くサーバーの機能に実装するには、主に識別します。 
  
|||
|:-----|:-----|
|関連するプロパティ  <br/> |dispidRemoteXP  <br/> |
|プロパティを設定します。  <br/> |PSETID_Remote  <br/> |
|長い ID (LID):  <br/> |0x00008F03  <br/> |
|データを入力します。  <br/> |PT_STRING8  <br/> |
|領域:  <br/> |リモート ・ メッセージ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージ クラスは IPM メッセージだけに関連します。リモートです。 Microsoft Outlook フォルダー関連の情報 (FAI) メッセージでは、特定の店舗へのダウンロードは、さまざまなアカウントのマッピングを保持するが、この情報をレジストリにも保存できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

