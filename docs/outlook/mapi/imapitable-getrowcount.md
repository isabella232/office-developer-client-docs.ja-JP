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
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328890"
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
  
> 予約語0である必要があります。
    
 _lルー count_
  
> 読み上げ表の行数へのポインターを指定します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行数が正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中であるため、行カウントの取得操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルで行数を計算できません。
    
MAPI_W_APPROX_COUNT 
  
> 呼び出しは成功しましたが、メモリの制約によって正確な行の数を特定できなかったため、おおよその行数が返されました。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**IMAPITable:: getrowcount**メソッドは、テーブル内の行の合計数を取得します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

テーブルの正確な行数を特定できない場合は、 _lMAPI_W_APPROX_COUNT count_パラメーターの内容で、および近似値の行数を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

データを取得するために[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出す前に、 **getrowcount**を使用して、テーブルに保持されている行の数を調べます。 テーブルに20行未満の行がある場合は、 **queryposition**を呼び出してテーブル全体を取得するのが安全です。 テーブルに20行を超える行がある場合は、複数の呼び出しを**queryposition**に設定し、呼び出しごとに取得する行数を制限することを検討してください。 
  
一部のテーブルは、 **getrowcount**をサポートせず、MAPI_E_NO_SUPPORT を返します。 **getrowcount**がサポートされていない場合、次の方法で[IMAPITable:: queryposition](imapitable-queryposition.md)を呼び出すことができます。 **queryposition**からの結果を使用して、現在の行と最後の行の間の関係を判断できます。 
  
一時的に行数を取得できないために**getrowcount**が MAPI_E_BUSY を返す場合は、 [IMAPITable:: waitforcompletion](imapitable-waitforcompletion.md)メソッドを呼び出します。 **waitforcompletion**が戻るときに、 **getrowcount**への呼び出しを再試行します。 非同期操作が進行中かどうかを検出する別の方法として、 [IMAPITable:: GetStatus](imapitable-getstatus.md)メソッドを呼び出し、 _lpultablestate_パラメーターの内容を確認する方法があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |copyfoldercontents  <br/> |mfcmapi は、 **IMAPITable:: getrowcount**メソッドを使用して、ソーステーブルにある行数を調べて、コピーを実行するためのメモリを割り当てることができるようにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

