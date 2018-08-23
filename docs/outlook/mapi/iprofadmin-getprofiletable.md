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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c942bdbf27590dde04b84970e345f265bc645045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801139"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**適用対象**: Outlook 
  
プロファイル テーブルのすべての利用可能なプロファイルに関する情報を格納するテーブルへのアクセスを提供します。
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]常に NULL を返します。
    
 _lppTable_
  
> [out]プロファイル テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイル テーブルが正常に取得しました。
    
## <a name="remarks"></a>注釈

**IProfAdmin::GetProfileTable**メソッドは、すべての利用可能なプロファイルの 1 つの行が含まれているプロファイルのテーブルへのアクセスを提供します。 各行の 2 つの列がある: プロファイルの表示名、およびプロファイルが既定値であるかどうかを示すフラグ。 
  
プロファイルが削除されている、またはを使用しているが、削除対象としてマークされている、プロファイル テーブルには含まれません。 プロファイル テーブルは静的です。テーブルでは、プロファイルの後の追加と削除は反映されません。 
  
プロファイルが存在しない場合、 **GetProfileTable**は、0 個の行を持つテーブルを返します。 
  
プロファイル テーブルの詳細については、[プロファイル テーブル](profile-tables.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI では、 **IProfAdmin::GetProfileTable**メソッドを使用して、新しいダイアログ ボックスに表示するプロファイル テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

