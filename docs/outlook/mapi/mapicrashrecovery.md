---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407215"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**適用対象**: Outlook 2013 | Outlook 2016 
  
**mapicrashrecovery**関数は、個人用フォルダーファイル (PST) またはオフラインフォルダーファイル (OST) の共有メモリの状態をチェックします。 メモリが一貫した状態にある場合、 **mapicrashrecovery**関数はデータをディスクに移動し、プロセスが終了するまで追加の読み取りまたは書き込みアクセスを禁止します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |olmapi32  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> 順番MAPI のクラッシュ回復を実行する方法を制御するために使用されるフラグです。 次のフラグを設定できます。
    
   - **mapicrash\_の回復**: pst または ost が一貫した状態にある場合は、データをディスクに移動し、pst または ost をロックして読み取りまたは書き込みのアクセスを禁止します。
    
   - **mapicrash\_CONTINUE**: デバッグのために pst または ost のロックを解除します。 **MAPICRASH_RECOVER**フラグを使用して**mapicrashrecovery**を正常に呼び出した後、mapicrash **\_** の**回復**を使用して、デバッグを続行できるようにします。 
    
   - **mapicrash\_SYSTEM_SHUTDOWN**: pst または ost が一貫した状態にある場合は、データをディスクに移動し、pst または ost をロックして読み取りまたは書き込みアクセスを禁止します。 pst または ost を、 **mapicrash\_の CONTINUE**を使用してロック解除することはできません。 **mapicrash\_の回復**と組み合わせて使用する必要があります。 
    
## <a name="remarks"></a>注釈

上位バイト (0xFF000000) は、プロバイダー固有のクラッシュ回復フラグ用に予約されています。
  
**WM_ENDSESSION**メッセージへの応答として、 **mapicrash\_の RECOVER**および**MAPICRASH_SYSTEM_SHUTDOWN**フラグを使用して、 **mapicrashrecovery**を呼び出します。 
  
## <a name="see-also"></a>関連項目

- [MAPI クラッシュ回復 API について](about-the-mapi-crash-recovery-api.md)
- [MAPI クラッシュ回復 API を使用する](how-to-use-the-mapi-crash-recovery-api.md)

