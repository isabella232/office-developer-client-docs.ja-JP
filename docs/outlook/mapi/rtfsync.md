---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ce90548a39ce33c795f68e513f3c178131b50b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591270"
---
# <a name="rtfsync"></a>RTFSync

**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチ テキスト形式 (RTF) メッセージ テキストがプレーン テキスト のバージョンと一致する必要があります。 RTF バージョンを読み取る前と RTF バージョンを変更した後に、この関数を呼び出す必要があります。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |RTF 対応のクライアント アプリケーションとメッセージ ストア プロバイダー  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>パラメーター

_lpMessage_
  
> [in]更新するメッセージへのポインター。
    
_ulFlags_
  
> [in]メッセージの RTF またはプレーン テキスト バージョンを示すために使用されるフラグのビットマスクが変更されました。 次のフラグを設定できます。
    
  - RTF_SYNC_BODY_CHANGED: メッセージのプレーン テキスト バージョンが変更されました。
      
  - RTF_SYNC_RTF_CHANGED: メッセージの RTF バージョンが変更されました。
    
  _ulFlags_ パラメーター内の他のすべてのビットは、将来の使用のために予約されています。 
    
_lpfMessageUpdated_
  
> [out]更新されたメッセージが存在するかどうかを示す変数へのポインター。 更新されたメッセージがある場合は TRUE、それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが見つからないか、FALSE の場合は、PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを読み取る前に **、RTFSync** 関数を RTF_SYNC_BODY_CHANGED フラグ セットで呼び出す必要があります。  
  
PR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで **STORE_RTF_OK** フラグが設定されていない場合、この関数は、PR_RTF_COMPRESSED を変更した後に RTF_SYNC_RTF_CHANGED フラグを設定して **呼び出す必要があります**。 
  
両方の **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) と PR_RTF_COMPRESSED変更されている場合は、両方のフラグ **を** 設定して **RTFSync** 関数を呼び出す必要があります。 
  
_lpfMessageUpdated_ パラメーターの値が TRUE に設定されている場合は、メッセージに対して [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。 **SaveChanges が** 呼び出されない場合、変更はメッセージに保存されません。 
  
メッセージ ストア プロバイダーは **、RTFSync** を使用して、PR_BODY **プロパティPR_RTF_COMPRESSED****維持できます**。 
  
詳細については、「メッセージ ストア プロバイダー [の RTF テキストのサポート」を参照してください](supporting-rtf-text-for-message-store-providers.md)。 
  
## <a name="see-also"></a>関連項目

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

