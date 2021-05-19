---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341700"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したコンテナーを既定のアドレス帳コンテナーとして確立します。
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]既定のアドレス帳コンテナーのエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 既定のアドレス帳コンテナーが正常に設定されました。
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **、SetDefaultDir** メソッドを呼び出して、新しい既定のアドレス帳コンテナーを確立します。 既定のコンテナーは、ユーザーがアドレス帳を最初に開いたときにアドレス帳に表示されるコンテナーです。 **SetDefaultDir は** 、既定のコンテナーをプロファイルのエントリとして保存します。 **SetDefaultDir** への別の呼び出しが同じセッションまたは別のセッションで行われたか、コンテナーが削除されるまで、コンテナーは既定のままです。 
  
> [!NOTE]
> [[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY]](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティは、[アドレス帳のオプション]**ダイアログの**[自動的に選択する] 設定に対応します。 このプロパティが IID_CAPONE_PROF プロファイル セクションに存在し **、true** に設定されている場合、アドレス帳ダイアログは **SetDefaultDir** で指定されたコンテナーに既定で設定されなくなりましたが、Microsoft [Outlook](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx)がダイアログが表示されたコンテキストに適したアドレス帳を選択します。 これにより、サードパーティのアドレス帳プロバイダーのエクスペリエンスが低下する可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI は **SetDefaultDir** メソッドを使用して、指定したアドレス帳コンテナーを既定のアドレス帳コンテナーにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

