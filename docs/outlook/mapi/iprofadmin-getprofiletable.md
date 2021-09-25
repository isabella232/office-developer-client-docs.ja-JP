---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9fa8107a551ed46d5b1790eb1965bf242cc79b2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556323"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
使用可能なすべてのプロファイルに関する情報を含むテーブルであるプロファイル テーブルへのアクセスを提供します。
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]常に NULL。
    
 _lppTable_
  
> [out]プロファイル テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイル テーブルが正常に取得されました。
    
## <a name="remarks"></a>注釈

**IProfAdmin::GetProfileTable** メソッドは、利用可能なプロファイルごとに 1 行を含むプロファイル テーブルへのアクセスを提供します。 各行には、プロファイルの表示名と、プロファイルが既定であるかどうかを示すフラグの 2 つの列があります。 
  
削除されたプロファイル、または使用されているが削除のマークが付いているプロファイルは、プロファイル テーブルには含まれません。 プロファイル テーブルは静的です。以降のプロファイルの追加および削除は、表には反映されません。 
  
プロファイルが存在しない場合 **、GetProfileTable は** 行が 0 のテーブルを返します。 
  
プロファイル テーブルの詳細については、「Profile [Tables」を参照してください](profile-tables.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI は **、IProfAdmin::GetProfileTable** メソッドを使用して、新しいダイアログ ボックスに表示するプロファイル テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

