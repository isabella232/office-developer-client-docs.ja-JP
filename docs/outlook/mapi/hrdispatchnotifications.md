---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385565"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォースは、キューに登録されたすべての通知のディスパッチします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
## <a name="return-value"></a>戻り値

S_OK
  
> すべてのキューに登録された通知がディスパッチされました。
    
MAPI_E_USER_CANCEL
  
> WM_QUIT、られる、または WM_ENDSESSION を受信しました。
    
MAPI_E_NOT_INITIALIZED
  
> MAPI は初期化されませんでした。
    
## <a name="remarks"></a>備考

**HrDispatchNotifications**関数は、MAPI メッセージのディスパッチを待たずに、MAPI 通知エンジンにキューイングされているすべての通知をディスパッチするときに発生します。 これにより、メモリの使用率に効果をもたらさないことができます。 詳細については、[強制的に通知](forcing-a-notification.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx)と[もないとき](https://msdn.microsoft.com/library/ms644934.aspx)の関数を使用してタイムアウト ループ内での通知メッセージの一部のアプリケーションを待ちます。 最速のプラットフォームはすべて、このようなアプリケーションがありますパフォーマンスが低下または通知の偶数進行を妨げています。 **HrDispatchNotifications**を使用して、コードを削減するだけでなく、パフォーマンスが向上します。 
  

