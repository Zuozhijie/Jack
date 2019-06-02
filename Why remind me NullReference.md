# Jack
//Ask  questions On GitHub,I‘m a new.

string uri = @"File:/// D:\Unity2019\AssetBundles\AssetBundle\cubewall.unity3d";
 UnityWebRequest request = UnityWebRequestAssetBundle.GetAssetBundle(uri,0);
 yield return request.SendWebRequest();
 AssetBundle ab = DownloadHandlerAssetBundle.GetContent(request);
 GameObject abPerfab = ab.LoadAsset<GameObject>("Wall");
 Instantiate(abPerfab);
