---
title: PidTagSubmitFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803615"
---
# <a name="pidtagsubmitflags-canonical-property"></a>PidTagSubmitFlags の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの送信に関する詳細情報を示すフラグのビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SUBMIT_FLAGS  <br/> |
|識別子:  <br/> |0x0E14  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

**PR_SUBMIT_FLAGS**ビットマスクについては、次のフラグの 1 つ以上を設定できます。 
  
SUBMITFLAG_LOCKED 
  
> MAPI スプーラーは、現在ロックされているメッセージを持ちます。 
    
SUBMITFLAG_PREPROCESS 
  
> メッセージでは、前処理が必要です。 MAPI スプーラーが終了するとこのメッセージを処理するには、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出すことができます。 メッセージ ストア プロバイダーは、クライアント ・ アプリケーションではなく、スプーラーでは、 **SubmitMessage**と呼ばれる、フラグをクリア、メッセージの送信を続行を認識します。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
