---
title: InfoPath フォームのデータにバインドできる ActiveX コントロールを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: InfoPath エディターで開くように設計された InfoPath フォームの中で、ActiveX コントロールをホストできます。これらのコントロールは、既存のもの (いくつかの制約があります) を利用するか、または InfoPath 用に特別に作成できます。
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799102"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>InfoPath フォームのデータにバインドできる ActiveX コントロールを作成する

InfoPath エディターで開くように設計された InfoPath フォームの中で、ActiveX コントロールをホストできます。これらのコントロールは、既存のもの (いくつかの制約があります) を利用するか、または InfoPath 用に特別に作成できます。
  
## <a name="write-an-activex-control"></a>ActiveX コントロールの作成

InfoPath の他のコントロールと同様に、ActiveX コントロールでも既存のコンポーネント オブジェクト モデル (COM) インターフェイスをサポートする必要があります。
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **初期化**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
ドキュメント オブジェクト モデル (DOM) のプロパティがコントロール内で変更されたときに InfoPath によってそれらのプロパティが更新されるように、次のインターフェイスをコントロールで実装する必要があります。
  
- **コネクション**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
また、コントロールとの統合をさらに密接にする、InfoPath 固有の 2 つの COM インターフェイスがあります。
  
- [IInfoPathControl](http://msdn.microsoft.com/en-us/library/bb264625.aspx)
    
- [IInfoPathControlSite](http://msdn.microsoft.com/en-us/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>InfoPath デザイン環境に ActiveX コントロールを追加する

[ **コントロール**] 作業ウィンドウの [ **カスタム コントロールの追加または削除**] コマンドを使用すると、 **カスタム コントロールの追加ウィザード**を実行してカスタム コントロールを追加できます。ウィザードでは、既に登録済みの ActiveX コントロールを選択したり、Office Marketplace でその他のカスタム コントロールを検索したりできます。コントロールを選択した後、次のことを指定できます。 
  
- CAB を指定して ActiveX コントロールをフォーム テンプレートと一緒にインストールする。
    
- バインディング プロパティを指定して XML にバインドする。
    
- ルールまたはデジタル署名に応答してコントロールを有効または無効にするのに使用されるプロパティを指定する。たとえば、XML が存在しない場合や条件付き書式を使用する場合などに役立ちます。
    
- データ型バインディングを指定する。
    
> [!NOTE]
> [!メモ] ActiveX コントロールを作成していて、既に InfoPath の [ **コントロール**] 作業ウィンドウに追加している場合は、InfoPath を閉じるまで ActiveX コントロールをビルドし直すことができなくなります。 
  
## <a name="deploy-an-activex-control"></a>ActiveX コントロールを展開する

ActiveX コントロールを配布するにはインストーラーを作成します。インストーラーでは、コントロールを目的のコンピューターにインストールし、InfoPath コントロール テンプレート (ICT) ファイルと CAB ファイルをユーザーのフォルダー \Users\\<ユーザー名\>\AppData\Local\Microsoft\InfoPath\Controls にコピーします。複数の開発者が、ActiveX コントロールを使用するフォームを共同で開発する場合は、InfoPath デザイン環境に追加されたコントロールをそれぞれの開発者が所有してください。そうしないと、InfoPath からコントロールのプロパティを変更できなくなります。
  
## <a name="see-also"></a>関連項目



演習 6: InfoPath 2003 で ActiveX コントロールを追加します。
  
[Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)

