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
  
**MAPICrashRecovery 関数は**、個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) 共有メモリの状態をチェックします。 メモリが一貫性のある状態にある場合 **、MAPICrashRecovery** 関数はデータをディスクに移動し、プロセスが終了するまで読み取りまたは書き込みアクセスを防止します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |olmapi32.dll  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> [in]MAPI クラッシュ回復の実行方法を制御するために使用されるフラグ。 次のフラグを設定できます。
    
   - **MAPICRASH \_RECOVER**: PST または OST が一貫性のある状態にある場合は、データをディスクに移動し、読み取りまたは書き込みアクセスを防ぐために PST または OST をロックします。
    
   - **MAPICRASH \_続行**: デバッグ用に PST または OST のロックを解除します。 **MAPICRASH_RECOVER** フラグを使用して **MAPICrashRecovery** を正常に呼び出した後 **、MAPICRASH \_ CONTINUE** フラグを使用して **MAPICrashRecovery** を呼び出して、デバッグを続行できます。 
    
   - **MAPICRASH \_SYSTEM_SHUTDOWN**: PST または OST が一貫性のある状態にある場合は、データをディスクに移動し、読み取りまたは書き込みアクセスを防ぐために PST または OST をロックします。 MAPICRASH CONTINUE を使用して PST または **OST のロックを解除 \_ することはできません**。 MAPICRASH RECOVER と組み **合わせて使用する \_ 必要があります**。 
    
## <a name="remarks"></a>注釈

上位バイト (0xFF000000) は、プロバイダー固有のクラッシュ回復フラグ用に予約されています。
  
**MAPICRASH RECOVER を使用して MAPICrashRecovery** を呼び出し、MAPICRASH_SYSTEM_SHUTDOWNメッセージに応答して **フラグをWM_ENDSESSION** します。 **\_**  
  
## <a name="see-also"></a>関連項目

- [MAPI クラッシュ回復 API について](about-the-mapi-crash-recovery-api.md)
- [MAPI クラッシュ回復 API を使用する](how-to-use-the-mapi-crash-recovery-api.md)

