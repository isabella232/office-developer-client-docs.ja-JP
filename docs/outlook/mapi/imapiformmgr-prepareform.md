---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416651"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
開くフォームをダウンロードします。
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番フォームのダウンロード中に表示される進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで MAPI_DIALOG フラグが設定されていない場合は無視されます。 
    
 _ulFlags_
  
> 順番フォームのダウンロード方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 状態を提供するユーザーインターフェイスを表示します。詳細については、ユーザーに確認します。 このフラグが設定されていない場合、ユーザーインターフェイスは表示されません。
    
 _pfrmiinfo_
  
> 順番フォームをダウンロードするためのフォーム情報オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォームビューアーは、 **imapiformmgr::P repareform**メソッドを呼び出して、フォームを開いてフォームコンテナーからダウンロードします。 ほとんどのフォーム閲覧者は**PrepareForm**を呼び出す必要はありません。このため、必要に応じて、 [imapiformmgr:: CreateForm](imapiformmgr-createform.md)メソッドと[imapiformmgr:: loadform](imapiformmgr-loadform.md)メソッドが**PrepareForm**を呼び出します。 
  
**PrepareForm**を使用して、ダイナミックリンクライブラリ (dll) およびフォームに関連付けられているその他のファイルを取得して、それらを変更できます。 変更されたフォームがフォームコンテナーに再び読み込まれる場合は、再インストールする必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

