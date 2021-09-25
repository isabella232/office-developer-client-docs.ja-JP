---
title: Update 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: 指定したフィールドに対して INSERT 操作または UPDATE 操作が試行されたかどうかを返します。
ms.openlocfilehash: 0ec2576a95c76be2f61abbd59c7de098a160c279
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614648"
---
# <a name="update-function-access-custom-web-app"></a>Update 関数 (Access カスタム Web アプリ)

指定したフィールドに対して INSERT 操作または UPDATE 操作が試行されたかどうかを返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

 **更新** (*列*) 
  
**Update 関数には**、次の引数が含まれます。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Column*  <br/> |INSERT 操作または UPDATE 操作をチェックするフィールドの名前。  <br/> |
   
## <a name="remarks"></a>注釈

**Update 関数** は、INSERT または UPDATE の試行が成功したかどうかに関係なく、TRUE を返します。 
  

