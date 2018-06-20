---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 24718c50d02da5d60a6594f56ea6100650fe9f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800748"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**適用されます**: Outlook 
  
ステータス テーブルを変更するには、新しい行を追加したり、既存の行を変更します。
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _あう_
  
> [in]新しいまたは変更された状態のテーブルの行に含まれるプロパティの数。 
    
 _lpColumnVals_
  
> [in]新しいまたは変更された状態のテーブルの行の列に含まれるプロパティを記述するプロパティ値の配列へのポインター。
    
 _ulFlags_
  
> [in]状態テーブルの行を定義する情報の処理方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
STATUSROW_UPDATE 
  
> 新しい行ではなく、既存の状態のテーブルの行を_lpColumnVals_が指す配列に含まれるプロパティをマージするための MAPI に指示します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 状態テーブルは正しく更新されました。
    
## <a name="remarks"></a>備考

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::ModifyStatusRow**メソッドを実装します。 サービス プロバイダーは、状態テーブルに行を追加するのにはログオン時に、行を更新するのにはセッション中に他の時間に**ModifyStatusRow**を呼び出します。 **ModifyStatusRow**は、状態テーブルを構築するために必要な情報を使用して MAPI を提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

既存の状態テーブルの行のプロパティを変更するのには、 **ModifyStatusRow**を呼び出すときは、STATUSROW_UPDATE フラグを設定します。 そう通知 MAPI が変更される列のみが、 _lpColumnVals_パラメーターに渡されています。 
  
クライアントは、状態オブジェクトにアクセスするのには、状態テーブルの情報を使用できます。 
  
状態テーブルの行を列に含める列の一覧については、[ステータス ・ テーブル](status-tables.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

