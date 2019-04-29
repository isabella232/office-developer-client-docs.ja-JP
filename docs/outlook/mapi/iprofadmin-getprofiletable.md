---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414646"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
利用可能なすべてのプロファイルについての情報を含むテーブルである、プロファイルテーブルへのアクセスを提供します。
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番常に NULL。
    
 _lpptable_
  
> 読み上げプロファイルテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルテーブルが正常に取得されました。
    
## <a name="remarks"></a>注釈

**IProfAdmin:: getprofiletable**メソッドはプロファイルテーブルへのアクセスを提供します。これには、使用可能なすべてのプロファイルに対応する1つの行が含まれています。 各行には、プロファイルの表示名、およびプロファイルが既定であるかどうかを示すフラグの2つの列のみがあります。 
  
削除されているか、使用されているが削除対象としてマークされているプロファイルは、プロファイルテーブルには含まれません。 プロファイルテーブルは静的です。後でプロファイルを追加または削除しても、テーブルには反映されません。 
  
プロファイルが存在しない場合、 **getprofiletable**は、行数が0のテーブルを返します。 
  
プロファイルテーブルの詳細については、「 [profile Tables](profile-tables.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onshowprofiles  <br/> |mfcmapi は、 **IProfAdmin:: getprofiletable**メソッドを使用して、新しいダイアログボックスに表示するプロファイルテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

