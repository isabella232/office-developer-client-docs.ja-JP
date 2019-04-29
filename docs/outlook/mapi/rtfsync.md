---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436210"
---
# <a name="rtfsync"></a>RTFSync

**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチテキスト形式 (RTF) のメッセージテキストがプレーンテキストバージョンと一致することを確認します。 rtf バージョンを読み取る前に、または rtf バージョンを変更した後に、この関数を呼び出す必要があります。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |RTF 対応クライアントアプリケーションとメッセージストアプロバイダー  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>パラメーター

_lpmessage_
  
> 順番更新するメッセージへのポインター。
    
_ulFlags_
  
> 順番メッセージの RTF またはプレーンテキストのバージョンが変更されたことを示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
  - RTF_SYNC_BODY_CHANGED: メッセージのテキスト形式のバージョンが変更されました。
      
  - RTF_SYNC_RTF_CHANGED: メッセージの RTF バージョンが変更されました。
    
  _ulflags_パラメーターの他のすべてのビットは、今後の使用のために予約されています。 
    
_lpfmessageupdated_
  
> 読み上げ更新されたメッセージがあるかどうかを示す変数へのポインター。 更新されたメッセージがある場合は TRUE、それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが存在しないか FALSE の場合は、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを読み取る前に、RTF_SYNC_BODY_ を使用して**rtfsync**関数を呼び出す必要があります。フラグセットが変更されました。 
  
STORE_RTF_OK フラグが**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで設定されていない場合、この関数は、 **PR_RTF_COMPRESSED**の変更後に RTF_SYNC_RTF_CHANGED フラグセットを使用して呼び出されます。 
  
**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) と**PR_RTF_COMPRESSED**の両方が変更されている場合は、両方の flags セットを使用して**rtfsync**関数を呼び出す必要があります。 
  
_lpfmessageupdated_パラメーターの値が TRUE に設定されている場合は、メッセージに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。 **SaveChanges**が呼び出されていない場合、変更はメッセージに保存されません。 
  
メッセージストアプロバイダーは、 **rtfsync**を使用して、 **PR_BODY**プロパティと**PR_RTF_COMPRESSED**プロパティを同期させておくことができます。 
  
詳細については、「[メッセージストアプロバイダー用の RTF テキストのサポート](supporting-rtf-text-for-message-store-providers.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

