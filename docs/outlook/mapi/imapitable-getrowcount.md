---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ebb926c340b194aae06bb057edf5a4bd1efe20ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630650"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の行の総数を返します。 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _lpulCount_
  
> [out]テーブル内の行数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行数が正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中で、行数の取得操作が開始されません。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは行数を計算できません。
    
MAPI_W_APPROX_COUNT 
  
> 呼び出しは成功しましたが、メモリの制約により正確な行数を決定できない可能性が高いので、おおよその行数が返されました。 この警告をテストするには、次のマクロ **HR_FAILED** します。 「エラー [処理のためのマクロの使用」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPITable::GetRowCount** メソッドは、テーブル内の行の総数を取得します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

テーブルの正確な行数を確認できない場合は  _、lpulCount_ パラメーター MAPI_W_APPROX_COUNTの値と近似行数を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GetRowCount を使用** して、データを取得するために [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出す前に、テーブルが保持する行の数を確認します。 テーブルに 20 行未満の行がある場合は **、QueryPosition** を呼び出してテーブル全体を取得しても安全です。 テーブル内に 20 行を超える行がある場合は **、QueryPosition** に対して複数の呼び出しを行い、各呼び出しで取得される行数を制限します。 
  
一部のテーブルは **GetRowCount をサポートしていないの** で、この値MAPI_E_NO_SUPPORT。 **GetRowCount が** サポートされていない場合は [、IMAPITable::QueryPosition](imapitable-queryposition.md)を呼び出す方法があります。 QueryPosition の結果 **を使用** して、現在の行と最後の行の関係を決定できます。 
  
**GetRowCount** が一MAPI_E_BUSY行数を取得することができないため、この値を返す場合は [、IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出します。 **WaitForCompletion が返** された場合は **、GetRowCount の呼び出しを再試行します**。 非同期操作が進行中かどうかを検出するもう 1 つの方法は [、IMAPITable::GetStatus](imapitable-getstatus.md) メソッドを呼び出し  _、lpulTableState_ パラメーターの内容を確認する方法です。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI は **IMAPITable::GetRowCount** メソッドを使用して、コピーを実行するためにメモリを割り当て可能なソース テーブル内の行数を決定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

