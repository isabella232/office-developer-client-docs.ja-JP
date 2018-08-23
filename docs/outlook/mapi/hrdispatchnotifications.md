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
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594699"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォースは、キューに登録されたすべての通知のディスパッチします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> すべてのキューに登録された通知がディスパッチされました。
    
MAPI_E_USER_CANCEL
  
> WM_QUIT、られる、または WM_ENDSESSION を受信しました。
    
MAPI_E_NOT_INITIALIZED
  
> MAPI は初期化されませんでした。
    
## <a name="remarks"></a>注釈

**HrDispatchNotifications**関数は、MAPI メッセージのディスパッチを待たずに、MAPI 通知エンジンにキューイングされているすべての通知をディスパッチするときに発生します。 これにより、メモリの使用率に効果をもたらさないことができます。 詳細については、[強制的に通知](forcing-a-notification.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx)と[もないとき](http://msdn.microsoft.com/en-us/library/ms644934.aspx)の関数を使用してタイムアウト ループ内での通知メッセージの一部のアプリケーションを待ちます。 最速のプラットフォームはすべて、このようなアプリケーションがありますパフォーマンスが低下または通知の偶数進行を妨げています。 **HrDispatchNotifications**を使用して、コードを削減するだけでなく、パフォーマンスが向上します。 
  

