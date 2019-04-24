---
title: DeleteRecord Data マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: DeleteRecord/レコードの削除アクションを使用して、レコードを削除できます。
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282116"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>DeleteRecord Data マクロアクション (Access カスタム web アプリ)

You can use the **DeleteRecord** action to delete a record. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**DeleteRecord** アクションの引数は次のとおりです。 
  
|**Arg1 と Arg2 の値**|**説明**|
|:-----|:-----|
|**Record Alias/レコードの別名** <br/> |削除するレコードを識別する文字列。 *Alias*引数が指定されていない場合は、カレントレコードが削除されます。  <br/> |
   
## <a name="remarks"></a>解説

**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。 
  
`[LastCreateRecordIdentity]`


