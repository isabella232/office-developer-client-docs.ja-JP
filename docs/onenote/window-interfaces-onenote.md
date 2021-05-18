---
title: ウィンドウ インターフェイス (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: WindowとWindowsのインターフェイスは、 OneNote 2013 API は OneNote ウィンドウを操作するユーザーを有効にするオブジェクトです。これらのオブジェクトでは、OneNote ウィンドウの集合を列挙し、特定のウィンドウのプロパティを変更することができます。
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317037"
---
# <a name="window-interfaces-onenote"></a>ウィンドウ インターフェイス (OneNote 2013)

**Window** と **Windows** のインターフェイスは、 OneNote 2013 API は OneNote ウィンドウを操作するユーザーを有効にするオブジェクトです。これらのオブジェクトでは、OneNote ウィンドウの集合を列挙し、特定のウィンドウのプロパティを変更することができます。 
  
## <a name="onenote-window-views"></a>OneNote ウィンドウ ビュー

OneNote ウィンドウ用に使用できる 4 つの表示モードを次に示します。 
  
- 通常のビュー： ノートブックとページのナビゲーション ウィンドウに表示されている既定の OneNote ウィンドウが表示されます。
    
- 完全なページの表示： 最小ユーザー インターフェイス (UI) であり、ノートブック、およびページのペインが表示されていないビューが表示されます。
    
- クイック注： 短いメモを取ることができます小さなウィンドウが表示されます。通常、Windows の通知領域に OneNote のアイコンをクイック ノートにアクセスするとは、OneNote の [ **表示**] タブからアクセスすることもできます。 
    
- デスクトップの端に-(タスク バーのような)、デスクトップの任意の辺に OneNote ウィンドウをドッキングすることができますが表示されます。このビューは、ウィンドウに収まるように、デスクトップのサイズを縮小します。1 つだけのウィンドウをドッキングするには、任意の時点と、ウィンドウは、デスクトップをブロックすることがなく常に表示します。 
    
次の図は、デスクトップのフル ページ ビュー、デスクトップへのドッキング ビュー、およびクイック メモの外観を示しています。
  
**OneNote のビュー**

![OneNote ビューとウィンドウ](media/ON15Con_views.jpg "OneNoteビュー")
  
## <a name="interfaces"></a>インターフェイス

このセクションは OneNote ウィンドウをプログラムで変更するのに使用できるメンバー、インターフェイスを示します。
  
### <a name="windows-interface"></a>Windowsインターフェイス

**Windows** インターフェイスは、一連の OneNote ウィンドウを開いてアクセスすることができます。 **Application.Windows** を使用してアクセス、OneNote の **Application** クラスのプロパティです。これは、OneNote ウィンドウの列挙型のセットを返します。 
  
**新しいプロパティ**

|**名前**|**型**|**説明**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |**Windows** セットには、 **Window** オブジェクトの数を取得します。  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |アクティブな OneNote ウィンドウの **Window** オブジェクトを取得します。  <br/> |
|**Items** <br/> |**Window** <br/> |渡されたインデックス値に対応する **Window** オブジェクトを返します。このプロパティに直接アクセスできません。オブジェクトを返すため、 **Window** 、 **Windows [(uint) index]** を使用します。 <br/> |
   
### <a name="window-interface"></a>ウィンドウ インターフェイス

**Window** インターフェイスは、各ウィンドウの特定のプロパティにアクセスすることができます。各 OneNote ウィンドウを列挙、 **Application** クラスの **Windows** プロパティを使用してアクセスできます。 
  
**新しいプロパティ**

|**名前**|**型**|**説明**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |取得またはウィンドウは、アクティブな OneNote ウィンドウであるかどうかを示す値を設定します。  <br/> |
|**Application** <br/> |**アプリケーション** <br/> |ウィンドウに関連付けられている、OneNote の **Application** オブジェクトを取得します。  <br/> |
|**CurrentPageId** <br/> |string  <br/> |ウィンドウの作業中の OneNote のページのオブジェクト ID を取得します。  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |ウィンドウの作業中の OneNote のセクションのオブジェクト ID を取得します。  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |オブジェクト ウィンドウの作業中の OneNote のセクション グループの ID を取得します。  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |ウィンドウの作業中の OneNote ノートブックのオブジェクト ID を取得します。  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |取得または、OneNote ウィンドウのドッキング場所を設定します。  <br/> |
|**FullPageView** <br/> |bool  <br/> |取得またはウィンドウが全体表示 (最小限の UI ビュー) であるかどうかを示す値を設定します。  <br/> |
|**SideNote** <br/> |bool  <br/> |取得またはをすばやくメモ ウィンドウだかどうかを示す値を設定します。  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |OneNote ウィンドウのハンドル ID を取得します。  <br/> |
   
**メソッド**
  
**Window** インターフェイスは、次の方法を使用するには、OneNote ウィンドウに指定したオブジェクトまたは指定した Url に移動します。 
  
**NavigateTo**

|||
|:-----|:-----|
|**説明** <br/> |OneNote ウィンドウの指定したオブジェクトに移動します。たとえば、セクション、ページ、およびページ内の要素のアウトラインに移動できます。  <br/> |
|**構文** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**パラメーター** <br/> | _bstrHierarchyObjectID_： に移動するオブジェクトの ID を OneNote の階層です。OneNote のノートブック、セクション、セクション グループ、またはページのオブジェクト ID を参照できます。 <br/>  _bstrObjectID_-OneNote の ID、特定のオブジェクトを OneNote のページ内に移動します。このパラメーターが設定されているユーザーがいない場合、ページ上の特定のオブジェクトに移動する、null にします。 <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**説明** <br/> |OneNote のリンクを渡された場合 (onenote://)、OneNote 内の対応する場所には、OneNote ウィンドウが開きます。 ただし、リンクが外部リンク (https://、file:// など) の場合は、セキュリティ ダイアログ ボックスが表示されます。 棄却に関する、OneNote でリンクを開くしようし、HResult.hrObjectDoesNotExist エラーが返されます。  <br/> |
|**構文** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**パラメーター** <br/> | _bstrUrl_-URL に移動します。  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**説明** <br/> |**dockLocation** と **ptMonitor** で、モニターで指定された場所にウィンドウをドッキングします。  <br/> |
|**構文** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**パラメーター** <br/> | _dockLocation_ - は、 OneNote 2013ウィンドウのドッキング場所を示します。  <br/>  _ptMonitor_ - x、y 座標、ウィンドウを監視する (省略可) を示しますに固定する必要があります。  <br/> |
   
## <a name="example"></a>例

次のコードでは、OneNote ウィンドウ ドッキング ウィンドウを反復処理します。ドッキング モードのウィンドウが存在しない場合の例は、作業中のウィンドウをドッキングします。アクティブなウィンドウが存在しない場合、コードは新しいドッキング ウィンドウを作成します。
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a>関連項目

- [OneNote 開発者用リファレンス](onenote-developer-reference.md)

