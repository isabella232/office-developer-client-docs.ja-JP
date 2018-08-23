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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6b07d794a8f54477c6706cb70af60f7f7ef57d49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595343"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**適用されます**: Outlook 2013 |Outlook 2016 
  
**MAPICrashRecovery**関数は、共有メモリを個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) の状態をチェックします。 メモリは、一貫性のある状態では、 **MAPICrashRecovery**関数はデータをディスクに移動して、プロセスが終了するまでに、さらに読み取りまたは書き込みアクセスを防ぐことが。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |olmapi32.dll  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>�p�����[�^�[

_ulFlags_
  
> [in]MAPI クラッシュ ・ リカバリの実行方法を制御するために使用するフラグです。 次のフラグを設定することができます。
    
   - **MAPICRASH\_回復**: pst ファイルまたは Ost が一貫性のある状態にある場合は、ディスクをロックする読み取りまたは書き込みアクセスを防止するには、pst ファイルまたは Ost のデータを移動します。
    
   - **MAPICRASH\_続行**: デバッグ用の pst ファイルまたは Ost のロックを解除します。 **MAPICRASH_RECOVER**フラグを使用して**MAPICrashRecovery**を呼び出して後で**MAPICrashRecovery**を呼び出す、 **MAPICRASH\_続行**フラグを続行するのにはデバッグを可能にします。 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: pst ファイルまたは Ost が一貫性のある状態にある場合は、ディスクをロックする読み取りまたは書き込みアクセスを防止するには、pst ファイルまたは Ost のデータを移動します。 Pst ファイルまたは Ost を使用してロックを解除することはできません**MAPICRASH\_続行**。 組み合わせて使用する必要があります**MAPICRASH\_回復**。 
    
## <a name="remarks"></a>注釈

上位バイト (0xFF000000) は、プロバイダーの特定のクラッシュ復旧のフラグは予約されています。
  
**MAPICrashRecovery**を呼び出して、 **MAPICRASH\_回復**と**WM_ENDSESSION**メッセージへの応答にフラグを**MAPICRASH_SYSTEM_SHUTDOWN** 。 
  
## <a name="see-also"></a>関連項目

- [MAPI クラッシュ回復 API について](about-the-mapi-crash-recovery-api.md)
- [MAPI クラッシュ回復 API を使用する](how-to-use-the-mapi-crash-recovery-api.md)

