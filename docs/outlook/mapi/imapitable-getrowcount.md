---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71178f1a531bd381387e0aa7fbacb02d4431a401
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584325"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブル内の行の合計数を返します。 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _lpulCount_
  
> [out]テーブル内の行の数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ローの数が正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作は、行カウントの取得操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは、行の数を計算できません。
    
MAPI_W_APPROX_COUNT 
  
> 呼び出しが成功したが、行数の正確な判断できませんでした可能性のあるメモリの制約があるために、おおよその行数が返されました。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 [エラー処理のためのマクロを使用する](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IMAPITable::GetRowCount**メソッドは、テーブル内の行の合計数を取得します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

テーブルの正確な行数を判断できない、戻り値の MAPI_W_APPROX_COUNT と、おおよその行が、 _lpulCount_パラメーターの内容をカウントします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

データを取得するために、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドの呼び出しを行う前にテーブルの行の数を検索する使用**な**を保持します。 テーブルに 20 未満の行がある場合は、テーブル全体を取得するために**QueryPosition**を呼び出しても安全です。 テーブルに 20 を超える行がある場合は、 **QueryPosition**を複数回呼び出すことを検討してくださいし、呼び出しのたびに取得される行の数を制限します。 
  
いくつかのテーブルをサポートしない**な**MAPI_E_NO_SUPPORT を取得します。 **な**はサポートされていない場合、 [IMAPITable::QueryPosition](imapitable-queryposition.md)を呼び出す別の方法を引き起こすことがあります。 **QueryPosition**から結果には、現在の行と最後の行の間の関係を指定できます。 
  
**な**に MAPI_E_BUSY が返されるは、行の数を取得するために一時的にできないため、ときに、 [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出します。 **WaitForCompletion**が返されるときは、**な**への呼び出しを再試行します。 非同期操作が進行中かどうかを検出するために別の方法では、 [IMAPITable::GetStatus](imapitable-getstatus.md)メソッドを呼び出すし、 _lpulTableState_パラメーターの内容を確認します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI では、 **IMAPITable::GetRowCount**メソッドを使用して、コピーを実行するのにはメモリの割り当てができるように、ソース テーブルでは、行の数を決定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

