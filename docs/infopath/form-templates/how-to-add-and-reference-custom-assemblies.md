---
title: カスタム アセンブリを追加および参照する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003 互換のフォーム テンプレート,カスタム アセンブリを使用する,アセンブリ [InfoPath 2007],InfoPath 2003 オブジェクト モデルを使用してカスタムを追加する
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: マネージ コードのフォーム テンプレート プロジェクトでカスタム アセンブリへの参照を追加すると、プロジェクトをコンパイルおよび発行したときに、そのアセンブリがフォーム テンプレート ファイル (.xsn) に含められます。
ms.openlocfilehash: 19b5f06231bb03cfac8b32b157e03956b5fc334e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303662"
---
# <a name="add-and-reference-custom-assemblies"></a>カスタム アセンブリを追加および参照する

マネージ コードのフォーム テンプレート プロジェクトでカスタム アセンブリへの参照を追加すると、プロジェクトをコンパイルおよび発行したときに、そのアセンブリがフォーム テンプレート ファイル (.xsn) に含められます。
  
## <a name="add-and-reference-a-custom-assembly"></a>カスタム アセンブリを追加および参照する

InfoPath プロジェクト システムがフォーム テンプレート ファイルに追加されるファイルを管理する方法と競合しないように、フォーム テンプレート プロジェクトの最上位フォルダーには、参照するカスタム アセンブリをコピーしないでください。既定では、このフォルダーのパス形式は < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*  となります。 
  
参照するカスタム アセンブリをプロジェクト フォルダー内で移動するには、メイン プロジェクト フォルダーの下にサブフォルダーを作成し、そのサブフォルダーにコピーしたカスタム アセンブリを参照する必要があります。ただし、参照するアセンブリのためのサブフォルダーを作成する必要はありません。参照するアセンブリがプロジェクトの最上位フォルダーになければ、プロジェクトをコンパイルおよび発行したときに、InfoPath プロジェクト システムによってアセンブリがフォーム テンプレート ファイル (.xsn) にコピーされます。
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>既定の場所からカスタム アセンブリを参照する

1. Visual Studio 2012 でフォーム テンプレート プロジェクトを開きます。
    
2. [ **プロジェクト**] メニューの [ **参照の追加**] をクリックします。
    
3. [ **参照**] タブで、アセンブリを探して選択し、[ **OK**] をクリックして参照を追加します。 
    
## <a name="see-also"></a>関連項目

#### <a name="tasks"></a>タスク

[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

