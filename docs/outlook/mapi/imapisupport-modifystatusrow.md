---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 19292d41e04b4a80d69ce68a1961c1deacbfde71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625428"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しい行を追加するか、既存の行を変更して、状態テーブルを変更します。
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _cValues_
  
> [in]新しいまたは変更された状態テーブル行に含めるプロパティの数。 
    
 _lpColumnVals_
  
> [in]新しいまたは変更された状態テーブル行に列として含めるプロパティを記述するプロパティ値の配列へのポインター。
    
 _ulFlags_
  
> [in]状態テーブル行を定義する情報の処理方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
STATUSROW_UPDATE 
  
> 新しい行ではなく  _、lpColumnVals_ が指す配列に含まれるプロパティを既存の状態テーブル行と結合する MAPI を指示します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 状態テーブルが正常に更新されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::ModifyStatusRow** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは、 **ログオン時に ModifyStatusRow** を呼び出して、状態テーブルに行を追加し、セッション中に行を更新します。 **ModifyStatusRow は** 、状態テーブルの構築に必要な情報を MAPI に提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ModifyStatusRow** STATUSROW_UPDATEを呼び出して、既存の状態テーブル行のプロパティを変更するときに、このフラグを設定します。 これにより、変更される列だけが  _lpColumnVals_ パラメーターに渡されるという MAPI が通知されます。 
  
クライアントは、状態テーブルの情報を使用して、status オブジェクトにアクセスできます。 
  
状態テーブルの行に含める必要がある列の完全な一覧については、「Status [Tables」を参照してください](status-tables.md)。
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

