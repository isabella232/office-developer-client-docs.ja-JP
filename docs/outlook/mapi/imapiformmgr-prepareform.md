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

 _ulUIParam_
  
> [in]フォームのダウンロード中に表示される進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _ulFlags_
  
> [in]フォームのダウンロード方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> ユーザー インターフェイスを表示して、状態を提供するか、ユーザーに詳細を求めるプロンプトを表示します。 このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。
    
 _pfrmiInfo_
  
> [in]ダウンロードするフォームのフォーム情報オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::P repareForm** メソッドを呼び出して、開くフォーム コンテナーからフォームをダウンロードします。 [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)メソッドと [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)メソッドの両方が必要に応じて **PrepareForm** を呼び出すので、ほとんどのフォーム ビューアーは **PrepareForm** を呼び出す必要はありません。 
  
**PrepareForm を使用して**、フォームに関連付けられた動的リンク ライブラリ (DLL) および他のファイルを取得して、それらを変更できます。 変更されたフォームがフォーム コンテナーに読み込まれた場合は、再インストールする必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

