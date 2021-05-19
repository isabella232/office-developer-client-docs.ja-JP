---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418016"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーション のユーザーがボタン コントロールをクリックすると、ダイアログ ボックスの表示やプログラムによる操作の開始などのタスクを実行します。
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _ulUIParam_
  
> [in]ボタン コントロールが表示されるダイアログ ボックスの親ウィンドウへのハンドル。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ボタン コントロールが正常にアクティブ化されました。
    
## <a name="remarks"></a>注釈

**IMAPIControl::Activate** メソッドは、ユーザーがボタン コントロールをクリックした後にタスクを実行します。 クリックが発生した後、表示テーブルの処理の一環として、MAPI は[IMAPIControl::GetState](imapicontrol-getstate.md)を最初に呼び出した後に Activate を呼び出し、ボタンが有効になっているかどうかを判断します。  
  
**Activate** および他の [IMAPIControl : IUnknown](imapicontroliunknown.md)メソッドを実装する方法の詳細については [、「Control Object Implementation」を参照してください](control-object-implementation.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

