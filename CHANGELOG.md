# Changelog

## 1.6.1 (2026-03-03)


### ⚠ BREAKING CHANGES

* **map:** Introduction of map instance caching needed a change to the DOM-Structure produced by the map component (added a div-element owned by the Map component to contain the map instance).
* **map:** The type passed to the `onProjectionChange` is changed from `MapCameraChangedEvent` to `MapEvent`, so there are no longer camera-props available for this event
* removed the `useStreetViewPanorama()` and `useDirectionsService()` hooks.
* The behaviour of the props controlling camera parameters (center, zoom, heading and tilt) changed. Unless you are using controlled props, you have to change the prop names from e.g. `center` to `defaultCenter` (the same goes for `zoom`, `heading` and `tilt`).
* removed MapProps.onLoadMap
* loading multiple libraries at once is no longer supported, changed the return type of useMapsLibrary.

### Features

* add `channel` prop to APIProvider ([#584](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/584)) ([4054bb4](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/4054bb48061d48f67a31911ed48b868b2604326a))
* add 3D map, marker and popover components ([#898](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/898)) ([e872e83](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e872e83f376fc91068fbcddb36b1447aa4d16cc1))
* add example for drawing tools ([#220](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/220)) ([9401a94](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9401a94c98b4b7b4952499888c5b2027397d6d18))
* add fetchAppCheckToken prop to APIProvider ([#913](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/913)) ([d1b4f2a](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/d1b4f2a1e98d622523d6b60b94354e7b4a5cbb4d))
* add hover events and anchor points to advanced markers ([#472](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/472)) ([4767822](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/4767822e8d9b6bf9bc329902f3156b657abd3c74))
* add new `onError` prop for api provider ([#541](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/541)) ([3149323](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/3149323633f47310737a6905faeab990ba757aef))
* add new prop InfoWindow.shouldFocus ([#254](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/254)) ([e6c6778](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e6c6778b3cb390175793e5edcb99de4648cd977a))
* add solution-channel parameter ([#334](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/334)) ([2abed12](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/2abed12de8baa221c9874b981a69a191742bd2bf))
* add StaticMap component with SSR support ([#633](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/633)) ([dfa6b5f](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/dfa6b5f593a1f8ff81bb953f4f1067f904660fb7))
* add TypeScript type definitions for Google Maps custom elements ([#857](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/857)) ([513aa3c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/513aa3c88b5a9090fc5e06b13f39049bc2ea13b6))
* **advanced-marker:** add style prop to add styles to content-element ([#337](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/337)) ([0558169](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/0558169c29c9f9b6da4caa939e3f52c472c58269))
* **advanced-marker:** add support for `clickable` option ([#341](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/341)) ([d48bd58](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/d48bd58b2d88ae0cff8b53f86761600e00b1182a))
* Allow &lt;Pin&gt; glyphs to be passed as children (close [#98](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/98)) ([#99](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/99)) ([3836c22](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/3836c22ee99e60d3c16547122e2495d8e5c4894c))
* **api-loader:** migrate to @googlemaps/js-api-loader ([#885](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/885)) ([60d277f](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/60d277fd75c1cec64178a68576302cdbbca6ad63))
* better handling for missing map configuration ([#308](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/308)) ([1030224](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/1030224d17e297a59c501aec5c92801d124e7304))
* cleanup map, remove onLoadMap prop ([9816b64](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9816b64df94ed50c9c526f8cdf57715c99502981))
* handle API-key errors in map-component ([#165](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/165)) ([dfc8c34](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/dfc8c3416e8df30a64834c5de2223ef6d946de19))
* implement props for all map-events with custom MapEvent type ([d0a69ec](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/d0a69ec9274c4c9325370f7bc1992d10a34cae7a))
* implement usage attribution ([#844](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/844)) ([028f48e](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/028f48e42b9564d65f2047496c972f887b38a0a1))
* **infowindow:** add `className` and `style` props ([9de7c2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9de7c2c53346258af6a4669d8e530d3259eedc76))
* **infowindow:** add missing options and events ([9de7c2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9de7c2c53346258af6a4669d8e530d3259eedc76))
* **infowindow:** add new headerContent prop ([#396](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/396)) ([e957e3c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e957e3cb87cd8fbb1ae5fefe6f3c7c92e6ddc76d)), closes [#378](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/378)
* **infowindow:** InfoWindow overhaul ([#335](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/335)) ([9de7c2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9de7c2c53346258af6a4669d8e530d3259eedc76))
* **map:** add padding option to defaultBounds ([#392](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/392)) ([586d01a](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/586d01ae2c4e1e942c705fb683abf0c25f440507))
* **map:** implement initial version of map-instance caching ([#349](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/349)) ([663019d](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/663019d1c54b2f6cf74088878d84400d2b6efccb))
* new MapControl component ([#51](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/51)) ([7a7c30a](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/7a7c30ae98e53e0f3008bd7fce902dca1150ba12))
* restore map state when changing mapId ([#213](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/213)) ([4e52ea6](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/4e52ea6f49a3073106f91771c3af0cd8785106ed))
* standalone examples (CodeSandbox) ([#48](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/48)) ([2f6afb5](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/2f6afb5f999270d2415a52e588c4b007dd730f25))
* update eslint-plugin-react-hooks ([#851](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/851)) ([ab7f5cb](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/ab7f5cb46f6b747633dca7e7c9cccd657a03e741))
* update map viewport when props are changed ([e3ef65d](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e3ef65de53600df89672dcf2351aa4430f364c30))
* updated AdvancedMarker anchoring implementation ([#841](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/841)) ([b4e9e96](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/b4e9e96d0ebef1b91197a9c1f06b47a817685f73))
* useMapsLibrary returns API object instead of boolean ([#26](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/26)) ([4020d46](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/4020d469e8e580b8f762b716589993e6b870445a))


### Bug Fixes

* add `loading=async` to maps API url ([a1b2e2a](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/a1b2e2a1633764bd51316e25ca14057a6ee255bd))
* add explicit type for exported function components ([#611](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/611)) ([98ef613](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/98ef6137d80620068f824d32bd10f80186543db9)), closes [#583](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/583)
* add map camera state tracking ([#84](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/84)) ([e191715](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e191715ef2710d181b97bbcde1a954f008155a75))
* add support Next.js 15 ([#609](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/609)) ([18131d1](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/18131d14382df53ed1f62df33c01a98098eff53c))
* add types to package exports ([#62](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/62)) ([77f5ed9](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/77f5ed93091131dc48b6a60bf69a967a64d9bc17))
* adjust advanced marker markup to fix anchoring & collision behavior ([#577](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/577)) ([b3460a2](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/b3460a23150346c0c1088abf7aeaba88c8d42998))
* **advanced-marker:** apply marker class when rendering a Pin ([#384](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/384)) ([732c290](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/732c2902978297f3d3b3c77fb9dee57c405b3724))
* **advanced-marker:** remove content element in cleanup ([#351](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/351)) ([a0a77f6](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/a0a77f611005cb99af06bba2a395961d38cdda92))
* allow AdvancedMarker to accept space-separated multiple class names ([#143](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/143)) ([09c8dd7](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/09c8dd71535ed3136b2f1cf81872936fbd496166))
* allow negative anchor values for AdvancedMarker ([#695](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/695)) ([cb03d49](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/cb03d49844b95f4c6e5a1a8f78eb61f6f3391619))
* api-loader didn't call callback on repeat load calls ([db1d03e](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/db1d03ebebb0fedaa3263cc6396aa00b4baadba0))
* avoid re-render on every importLibrary() call ([#135](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/135)) ([3c15c02](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/3c15c02ef3b34b944a0c7d6703c9d375ba9b07aa))
* avoid unnecessary state-updates in api-provider ([#551](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/551)) ([6b61bf6](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/6b61bf61cf685cbcaf46b7f449ceee98278173a9))
* better handling for `clickable` prop in AdvancedMarker ([#906](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/906)) ([ea7dae9](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/ea7dae9f4852100f17b0093369ead8d3497155dd))
* **custom-element-types:** update type definitions for boolean values ([1796286](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/1796286293c24b38aceac1159de56ba3bbe7e115))
* **deps-dev:** bump react, react-dom and corresponding types ([#650](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/650)) ([6279278](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/62792785c0f5c81461e028783d2533ad628dc185))
* **docs:** use correct spelling of JavaScript ([#312](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/312)) ([d72cb87](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/d72cb87ef0ac103027d80e4f8c4977d40b5068d4))
* don't use potentially unreliable addListener functions ([#158](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/158)) ([f7783cc](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/f7783cc8e89c22483297c81654df98cbc6652e02))
* empty commit to trigger release-please ([e92eeaa](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e92eeaa5e204c390757469dc7a30628394794769))
* ensure proper type inference of APILoadingStatus ([#747](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/747)) ([8a46e65](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/8a46e6597aba7d73e3398fe8197c10ed50c29aae))
* export api-loading-status types ([#231](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/231)) ([263389c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/263389cca93321b0e0e68b83524bd99d469c331d)), closes [#230](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/230)
* export event-types ([#167](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/167)) ([fb3f227](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/fb3f227dc2330e234ac3546d70d3ef900f5952fd))
* export type properly ([#170](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/170)) ([91ffb04](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/91ffb040234b88e89380b0d3ab2990c0a8c7086e))
* improve types ColorScheme and RenderingType ([#675](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/675)) ([8b42e67](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/8b42e675d9bd1740cecc01c75a0b289a9451d7c5))
* **info-window:** fix reappearing InfoWindows ([#393](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/393)) ([83f9b73](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/83f9b73ccf4a124f07ad75a125a760d730d2e289))
* infowindow double rendering and eslint warnings ([#185](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/185)) ([07ed25d](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/07ed25d8a253325b75b957efaf5d57f0d5f206ab))
* InfoWindow.shouldFocus doesn't work with false as value ([#278](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/278)) ([e6d3647](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e6d36477f58c8023cc6511597ae30a8bb85170b9))
* **infowindow:** add missing cleanup for infowindow ([9de7c2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9de7c2c53346258af6a4669d8e530d3259eedc76))
* **infowindow:** better dependency checks, using `useDeepCompareEffect` where needed ([9de7c2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9de7c2c53346258af6a4669d8e530d3259eedc76))
* **infowindow:** removed unneeded dependency in infowindow hooks ([9de7c2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9de7c2c53346258af6a4669d8e530d3259eedc76))
* **infowindow:** replace useDeepCompareEffect with useEffect ([#786](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/786)) ([f92f5e7](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/f92f5e7527e8bc272870c80d8ff9004318a7a4a2))
* introduce useEffectEvent to improve stability of event handlers ([#866](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/866)) ([e1053bc](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e1053bc3c9786ed79aa54da5abb9fdf61ab428a9))
* map controls crashing when invalid key is provided ([#290](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/290)) ([95bb16b](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/95bb16ba6ca810e508a01dadc0390dd72109e715))
* **map:** add support for new and missing mapOptions ([#501](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/501)) ([0cf12c2](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/0cf12c2d156ac9fe0cf55f18e6bd34d5bef57a2a))
* **map:** change event-type of projectionChanged event to MapEvent ([#346](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/346)) ([dc3b233](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/dc3b23334102e5b2546c42b858a7c14ef76f9a1f))
* **map:** improve reuseMaps reliability after remounting ([#920](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/920)) ([de2b422](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/de2b42264c35a8c4307d40b23bc34759213f2da5))
* **map:** remove [@ts-expect-error](https://github.com/ts-expect-error) after @types/google.maps update ([042c785](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/042c785ebfa80ece002bee95727f7f3a64823869))
* **map:** set container position to relative ([#356](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/356)) ([3ff9b33](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/3ff9b3315eb5dcc50ead88beb2fbd3685f1d82ec))
* **map:** set other container position to relative ([#357](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/357)) ([82f4e4b](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/82f4e4b67e50502925cdc380db134816d6f3522a))
* **map:** undefined rendering-type and color-scheme ([#515](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/515)) ([528458b](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/528458bb0ff33ad1b5920af01f1c7e16df0b31e9))
* markers not removed in strict mode ([#15](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/15)) ([9a9c586](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/9a9c586eeeb75dbd3aa548a48c155cd610f4115b)), closes [#14](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/14)
* memoize context-values to avoid excessive re-renders ([#287](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/287)) ([b067b72](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/b067b72568d8e79e0d6ba06e1d3df259e13c3918)), closes [#285](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/285)
* more efficient useMemoized hook and fixed infowindow issues ([#903](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/903)) ([b6c0963](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/b6c0963a18e837fd7f867deaa4254acf251613c1))
* move @types/google.maps to dependencies ([#115](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/115)) ([e415f1f](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/e415f1f1b4a4874d1c1cec83d7d9f951fd84a7bc)), closes [#106](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/106)
* omit map prop from markers ([#305](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/305)) ([dc08cd2](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/dc08cd26962dc805af80870e87c3d063a04db355))
* output an error when useMap is called outside APIProvider ([#117](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/117)) ([763d8b6](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/763d8b6db80e2c035a67d9566d4354f808a32fbc))
* prevent passing empty parameters to ApiLoader ([#193](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/193)) ([373d10d](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/373d10dc1a52f879112619e9e6d2d8ddff887ebe))
* remove deep-link into fast-deep-equal package ([#208](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/208)) ([4e3680b](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/4e3680bdd3093008211ca722e7ff0a1ff5a558eb))
* remove explicit types for components using forwardRef ([#620](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/620)) ([6ed2fcd](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/6ed2fcd08f2c3e9d5b770d5665ce45374afa441d)), closes [#619](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/619) [#617](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/617)
* replace prop `gmpDraggable` with `draggable` in AdvancedMarker ([#53](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/53)) ([6b39cf6](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/6b39cf618f7fdca6e929bb4106a2dbfdfc23f4fd))
* **static-maps:** remove path grouping by style ([#809](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/809)) ([cfd69df](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/cfd69df48e5f5e6c204a81c96b207616a603ab1d))
* trigger release for new library function from commit 31f2655 ([a94ec7b](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/a94ec7b0b9e650a1dd95bfbfee53b5cf57f988cd))
* trigger release-please action ([3f73b44](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/3f73b44679d0fef4c782483b82834748670d9c0c))
* **types:** add new PinElement and PinElementOptions types to augmentations ([35d5aa1](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/35d5aa123cad748f05f40af176b672c34c083739))
* **types:** add types-reference to google.maps ([#520](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/520)) ([65f95a9](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/65f95a90c6e954bbe6f15fd886c6ebac6604336e)), closes [#519](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/519)
* **types:** inline PlaceContextualElementOptions in types for 'gmp-place-contextual' ([3cfb08e](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/3cfb08e14e0d8b1e887768af5f81447b76e170fa))
* Update calc clusters to happen after Idle event - reduces issue 563 ([#806](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/806)) ([ca8b3ec](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/ca8b3ec1141b2d179762917c43a4fdd11e6a78db))
* update ControlPosition values ([#71](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/71)) ([0f5a3ee](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/0f5a3ee07e1fd1fc05120ecbb2fa4e16df4fea81))
* update usage of useMapsLibrary in AdvancedMarker ([#55](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/55)) ([35e59d5](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/35e59d57535f35f28d1e1af890f7e9504615deb6))
* update useMapsLibrary hook to include maps3d ([734fd14](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/734fd142858e1ac6da2ff4535a9f31988d331ffb))
* use deep compare effect to prevent infowindow close ([#642](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/642)) ([ad9ea2c](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/ad9ea2cd6932b8b34d0eae5ad0cfd3164d71de4e))
* use moveCamera and useLayoutEffect for faster map-updates ([2960285](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/29602853c675790dfc79dd6faebdb5651737b965))
* use parameter `v` instead of `version` ([721a671](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/721a67181aa2e19f744dead924952732839720c1))


### Miscellaneous Chores

* add registry-url to release action ([7ded49e](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/7ded49e802142b9f6aafa14bd2d670f6e1ea26f9))
* add tslib as devDependency ([#854](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/854)) ([ec2ceff](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/ec2ceff7c5999068e51500c983ca59959bd53a39))
* tag 1.0.0 release ([8c71810](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/8c718100f3836f995fc5d813172fd3aa05027d01))


### Code Refactoring

* improved state-handling implementation ([#181](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/181)) ([f45ac8a](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/f45ac8a312616edda4020f9a79d6b02bbbd82d32))
* remove obsolete hooks ([#219](https://github.com/anthonytran550-ui/tech-react-google-map-integration/issues/219)) ([0c1b6de](https://github.com/anthonytran550-ui/tech-react-google-map-integration/commit/0c1b6defe030edd9dd342f6ce964f8ff2e689c5b))

## [1.7.1](https://github.com/visgl/react-google-maps/compare/v1.7.0...v1.7.1) (2025-11-03)


### Bug Fixes

* **types:** add new PinElement and PinElementOptions types to augmentations ([3751d0d](https://github.com/visgl/react-google-maps/commit/3751d0d76a884fe76cb8bd23a993720416932c03))
* **types:** inline PlaceContextualElementOptions in types for 'gmp-place-contextual' ([0626be2](https://github.com/visgl/react-google-maps/commit/0626be24df8deb98b4779a121da6fbdb5023793d))

## [1.7.0](https://github.com/visgl/react-google-maps/compare/v1.6.1...v1.7.0) (2025-10-30)


### Features

* add TypeScript type definitions for Google Maps custom elements ([#857](https://github.com/visgl/react-google-maps/issues/857)) ([a946a36](https://github.com/visgl/react-google-maps/commit/a946a36ab41b092631987c04bebcd34ad4f84aa0))


### Bug Fixes

* **custom-element-types:** update type definitions for boolean values ([8db4ad0](https://github.com/visgl/react-google-maps/commit/8db4ad07c285056842e50e69a7866f3578f4100f))
* update useMapsLibrary hook to include maps3d ([bd218bb](https://github.com/visgl/react-google-maps/commit/bd218bb65f8a308f59cbce16cce32019c27101e6))

## [1.6.1](https://github.com/visgl/react-google-maps/compare/v1.6.0...v1.6.1) (2025-10-23)


### Features

* update eslint-plugin-react-hooks ([#851](https://github.com/visgl/react-google-maps/issues/851)) ([6ebe344](https://github.com/visgl/react-google-maps/commit/6ebe344d4baf36cf18924037dec43b82cf9b5561))


### Miscellaneous Chores

* add tslib as devDependency ([#854](https://github.com/visgl/react-google-maps/issues/854)) ([fe42240](https://github.com/visgl/react-google-maps/commit/fe42240abbca9ef30d247759bccfdbb93067ae45))

## [1.6.0](https://github.com/visgl/react-google-maps/compare/v1.5.5...v1.6.0) (2025-10-21)


### Features

* implement usage attribution ([#844](https://github.com/visgl/react-google-maps/issues/844)) ([af36b8f](https://github.com/visgl/react-google-maps/commit/af36b8feee4acdf44ee17a73e962a7ea062e72db))
* updated AdvancedMarker anchoring implementation ([#841](https://github.com/visgl/react-google-maps/issues/841)) ([d7b128e](https://github.com/visgl/react-google-maps/commit/d7b128e132fbb76855bcf56f1947796480a97705))

## [1.5.5](https://github.com/visgl/react-google-maps/compare/v1.5.4...v1.5.5) (2025-08-07)


### Bug Fixes

* **static-maps:** remove path grouping by style ([#809](https://github.com/visgl/react-google-maps/issues/809)) ([d1f499e](https://github.com/visgl/react-google-maps/commit/d1f499e6089086e40265c9b21c6a318d292e2f9e))
* Update calc clusters to happen after Idle event - reduces issue 563 ([#806](https://github.com/visgl/react-google-maps/issues/806)) ([bed6ccd](https://github.com/visgl/react-google-maps/commit/bed6ccd31911ac82decc758bd4ecee0a18fe492f))

## [1.5.4](https://github.com/visgl/react-google-maps/compare/v1.5.3...v1.5.4) (2025-07-06)


### Bug Fixes

* **infowindow:** replace useDeepCompareEffect with useEffect ([#786](https://github.com/visgl/react-google-maps/issues/786)) ([1b25e80](https://github.com/visgl/react-google-maps/commit/1b25e80107ea7589c2354d6c44e88761fd50d12f))

## [1.5.3](https://github.com/visgl/react-google-maps/compare/v1.5.2...v1.5.3) (2025-06-05)


### Bug Fixes

* ensure proper type inference of APILoadingStatus ([#747](https://github.com/visgl/react-google-maps/issues/747)) ([2c59d59](https://github.com/visgl/react-google-maps/commit/2c59d59b475b9bc1eef7d7f7bd9b08c2d215a3cb))

## [1.5.2](https://github.com/visgl/react-google-maps/compare/v1.5.1...v1.5.2) (2025-03-13)


### Bug Fixes

* allow negative anchor values for AdvancedMarker ([#695](https://github.com/visgl/react-google-maps/issues/695)) ([d2de370](https://github.com/visgl/react-google-maps/commit/d2de370d4c938293b24b662bb333b2db40e14923))

## [1.5.1](https://github.com/visgl/react-google-maps/compare/v1.5.0...v1.5.1) (2025-01-28)


### Bug Fixes

* improve types ColorScheme and RenderingType ([#675](https://github.com/visgl/react-google-maps/issues/675)) ([785927a](https://github.com/visgl/react-google-maps/commit/785927a9b69e6a2c08ab013f607270d0dc0fc653))

## [1.5.0](https://github.com/visgl/react-google-maps/compare/v1.4.3...v1.5.0) (2025-01-10)


### Features

* add StaticMap component with SSR support ([#633](https://github.com/visgl/react-google-maps/issues/633)) ([55acea2](https://github.com/visgl/react-google-maps/commit/55acea2a0b82727e487ee30fb788a05ba7dce153))

## [1.4.3](https://github.com/visgl/react-google-maps/compare/v1.4.2...v1.4.3) (2025-01-07)


### Bug Fixes

* **deps-dev:** bump react, react-dom and corresponding types ([#650](https://github.com/visgl/react-google-maps/issues/650)) ([02fe28f](https://github.com/visgl/react-google-maps/commit/02fe28fdc0e69a3ab0b3e8555b156b4c36d7c75c))
* use deep compare effect to prevent infowindow close ([#642](https://github.com/visgl/react-google-maps/issues/642)) ([bfa85c1](https://github.com/visgl/react-google-maps/commit/bfa85c177796ac05cb626590c2467a31edab86eb))

## [1.4.2](https://github.com/visgl/react-google-maps/compare/v1.4.1...v1.4.2) (2024-11-28)


### Bug Fixes

* remove explicit types for components using forwardRef ([#620](https://github.com/visgl/react-google-maps/issues/620)) ([8448a33](https://github.com/visgl/react-google-maps/commit/8448a336fdd2e489493bc40068bfa58d23267409)), closes [#619](https://github.com/visgl/react-google-maps/issues/619) [#617](https://github.com/visgl/react-google-maps/issues/617)

## [1.4.1](https://github.com/visgl/react-google-maps/compare/v1.4.0...v1.4.1) (2024-11-22)


### Bug Fixes

* add explicit type for exported function components ([#611](https://github.com/visgl/react-google-maps/issues/611)) ([a5b0359](https://github.com/visgl/react-google-maps/commit/a5b035986872b3abb8c28d6659034c2a897476a3)), closes [#583](https://github.com/visgl/react-google-maps/issues/583)
* add support Next.js 15 ([#609](https://github.com/visgl/react-google-maps/issues/609)) ([0e673c2](https://github.com/visgl/react-google-maps/commit/0e673c262a0a704a0d85a7f34cf4409965d11a8b))

## [1.4.0](https://github.com/visgl/react-google-maps/compare/v1.3.0...v1.4.0) (2024-10-24)


### Features

* add `channel` prop to APIProvider ([#584](https://github.com/visgl/react-google-maps/issues/584)) ([6aa38e5](https://github.com/visgl/react-google-maps/commit/6aa38e52a2cf0cc856167489b879871622c74ea8))


### Bug Fixes

* adjust advanced marker markup to fix anchoring & collision behavior ([#577](https://github.com/visgl/react-google-maps/issues/577)) ([97a98b2](https://github.com/visgl/react-google-maps/commit/97a98b2a04b896a892351a178fecafa665c03113))

## [1.3.0](https://github.com/visgl/react-google-maps/compare/v1.2.0...v1.3.0) (2024-09-30)


### Features

* add new `onError` prop for api provider ([#541](https://github.com/visgl/react-google-maps/issues/541)) ([bbe5709](https://github.com/visgl/react-google-maps/commit/bbe5709e1420e7260234b11a7749ed9b7804e9b7))


### Bug Fixes

* avoid unnecessary state-updates in api-provider ([#551](https://github.com/visgl/react-google-maps/issues/551)) ([46068c9](https://github.com/visgl/react-google-maps/commit/46068c9b3f3e930d464e2314181e2f6ed32a9aa7))

## [1.2.0](https://github.com/visgl/react-google-maps/compare/v1.1.3...v1.2.0) (2024-09-16)


### Features

* add hover events and anchor points to advanced markers ([#472](https://github.com/visgl/react-google-maps/issues/472)) ([cc4a397](https://github.com/visgl/react-google-maps/commit/cc4a397f0ed2af12a28c21db6afad3a946527131))

## [1.1.3](https://github.com/visgl/react-google-maps/compare/v1.1.2...v1.1.3) (2024-09-08)


### Bug Fixes

* **types:** add types-reference to google.maps ([#520](https://github.com/visgl/react-google-maps/issues/520)) ([ed19636](https://github.com/visgl/react-google-maps/commit/ed196365821d6ac8b97baa1a900842990f1959f2)), closes [#519](https://github.com/visgl/react-google-maps/issues/519)

## [1.1.2](https://github.com/visgl/react-google-maps/compare/v1.1.1...v1.1.2) (2024-09-06)


### Bug Fixes

* **map:** undefined rendering-type and color-scheme ([#515](https://github.com/visgl/react-google-maps/issues/515)) ([c288d15](https://github.com/visgl/react-google-maps/commit/c288d15e2b4bfa5d952ae06c1f586888987f86c7))

## [1.1.1](https://github.com/visgl/react-google-maps/compare/v1.1.0...v1.1.1) (2024-09-02)


### Bug Fixes

* **map:** add support for new and missing mapOptions ([#501](https://github.com/visgl/react-google-maps/issues/501)) ([f22af50](https://github.com/visgl/react-google-maps/commit/f22af50793622c2bee0508a4b57307dd18302d1b))
* **map:** remove [@ts-expect-error](https://github.com/ts-expect-error) after @types/google.maps update ([deb2bc7](https://github.com/visgl/react-google-maps/commit/deb2bc733800cb99ad8edeb30059ad050a16ee86))

## [1.1.0](https://github.com/visgl/react-google-maps/compare/v1.0.2...v1.1.0) (2024-06-17)


### Features

* **infowindow:** add new headerContent prop ([#396](https://github.com/visgl/react-google-maps/issues/396)) ([0d40c81](https://github.com/visgl/react-google-maps/commit/0d40c81fe0d850accccf031bfb4f6f7412eea73a)), closes [#378](https://github.com/visgl/react-google-maps/issues/378)
* **map:** add padding option to defaultBounds ([#392](https://github.com/visgl/react-google-maps/issues/392)) ([9dc65dc](https://github.com/visgl/react-google-maps/commit/9dc65dc36c1d3efb17ebcfa55da3b2f3909eb63f))

## [1.0.2](https://github.com/visgl/react-google-maps/compare/v1.0.1...v1.0.2) (2024-05-30)


### Bug Fixes

* **info-window:** fix reappearing InfoWindows ([#393](https://github.com/visgl/react-google-maps/issues/393)) ([dc51eb9](https://github.com/visgl/react-google-maps/commit/dc51eb979e5db6fb57a07d52efa36ef03e83dfcf))

## [1.0.1](https://github.com/visgl/react-google-maps/compare/v1.0.0...v1.0.1) (2024-05-27)


### Bug Fixes

* **advanced-marker:** apply marker class when rendering a Pin ([#384](https://github.com/visgl/react-google-maps/issues/384)) ([e8a4cc3](https://github.com/visgl/react-google-maps/commit/e8a4cc3aca92e92c20c1e99ba19fee7d713f4785))

## [1.0.0](https://github.com/visgl/react-google-maps/compare/v0.11.2...v1.0.0) (2024-05-11)


### Miscellaneous Chores

* tag 1.0.0 release ([afb67a7](https://github.com/visgl/react-google-maps/commit/afb67a7b076e83c025a147d488a93c33150c5b15))

## [0.11.2](https://github.com/visgl/react-google-maps/compare/v0.11.1...v0.11.2) (2024-05-10)


### Bug Fixes

* **map:** set other container position to relative ([#357](https://github.com/visgl/react-google-maps/issues/357)) ([8e77d70](https://github.com/visgl/react-google-maps/commit/8e77d70c272ac243c5d53f3dd6c02f508104226f))

## [0.11.1](https://github.com/visgl/react-google-maps/compare/v0.11.0...v0.11.1) (2024-05-10)


### Bug Fixes

* **advanced-marker:** remove content element in cleanup ([#351](https://github.com/visgl/react-google-maps/issues/351)) ([128df87](https://github.com/visgl/react-google-maps/commit/128df8730b7e1549e530a108192e7bae0699f199))
* **map:** set container position to relative ([#356](https://github.com/visgl/react-google-maps/issues/356)) ([7fa2b71](https://github.com/visgl/react-google-maps/commit/7fa2b711952a2472c409c38cd39edc1866cecbe3))

## [0.11.0](https://github.com/visgl/react-google-maps/compare/v0.10.0...v0.11.0) (2024-05-08)


### ⚠ BREAKING CHANGES

* **map:** Introduction of map instance caching needed a change to the DOM-Structure produced by the map component (added a div-element owned by the Map component to contain the map instance).
* **map:** The type passed to the `onProjectionChange` is changed from `MapCameraChangedEvent` to `MapEvent`, so there are no longer camera-props available for this event

### Features

* **advanced-marker:** add support for `clickable` option ([#341](https://github.com/visgl/react-google-maps/issues/341)) ([ca96e54](https://github.com/visgl/react-google-maps/commit/ca96e540a2117f7437745e8e1f71f83ef6c04e25))
* **map:** implement initial version of map-instance caching ([#349](https://github.com/visgl/react-google-maps/issues/349)) ([4a6e83a](https://github.com/visgl/react-google-maps/commit/4a6e83a26f06131baac288e3474d0e3163715f92))


### Bug Fixes

* **map:** change event-type of projectionChanged event to MapEvent ([#346](https://github.com/visgl/react-google-maps/issues/346)) ([83f9309](https://github.com/visgl/react-google-maps/commit/83f93091c858663b0183dd62bdc212a246013072))

## [0.10.0](https://github.com/visgl/react-google-maps/compare/v0.9.0...v0.10.0) (2024-05-03)


### Features

* add solution-channel parameter ([#334](https://github.com/visgl/react-google-maps/issues/334)) ([f93e43e](https://github.com/visgl/react-google-maps/commit/f93e43ee444a86dbc1b594d0c256229e6d207957))
* **advanced-marker:** add style prop to add styles to content-element ([#337](https://github.com/visgl/react-google-maps/issues/337)) ([e942fb5](https://github.com/visgl/react-google-maps/commit/e942fb5f5543a0a27e9987ee4324825958f08fdf))
* **infowindow:** add `className` and `style` props ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** add missing options and events ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** InfoWindow overhaul ([#335](https://github.com/visgl/react-google-maps/issues/335)) ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))


### Bug Fixes

* **infowindow:** add missing cleanup for infowindow ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** better dependency checks, using `useDeepCompareEffect` where needed ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** removed unneeded dependency in infowindow hooks ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))

## [0.9.0](https://github.com/visgl/react-google-maps/compare/v0.8.3...v0.9.0) (2024-04-18)


### Features

* better handling for missing map configuration ([#308](https://github.com/visgl/react-google-maps/issues/308)) ([b318d67](https://github.com/visgl/react-google-maps/commit/b318d676088e6f0ef787ffa911c552a12ecb4895))


### Bug Fixes

* **docs:** use correct spelling of JavaScript ([#312](https://github.com/visgl/react-google-maps/issues/312)) ([f38d3c4](https://github.com/visgl/react-google-maps/commit/f38d3c4004663fd1850c00dca7ddfb7e92b8d5cf))
* omit map prop from markers ([#305](https://github.com/visgl/react-google-maps/issues/305)) ([8a38acf](https://github.com/visgl/react-google-maps/commit/8a38acf04ab665bbeeeef87a87d195bcbf44ccea))

## [0.8.3](https://github.com/visgl/react-google-maps/compare/v0.8.2...v0.8.3) (2024-04-04)


### Bug Fixes

* api-loader didn't call callback on repeat load calls ([743878a](https://github.com/visgl/react-google-maps/commit/743878a33abe2b0fb6bfe96377df07066536e51e))
* map controls crashing when invalid key is provided ([#290](https://github.com/visgl/react-google-maps/issues/290)) ([5052dfb](https://github.com/visgl/react-google-maps/commit/5052dfbf3735ff07319b7bd7108ae9448b0c2840))

## [0.8.2](https://github.com/visgl/react-google-maps/compare/v0.8.1...v0.8.2) (2024-03-29)


### Bug Fixes

* memoize context-values to avoid excessive re-renders ([#287](https://github.com/visgl/react-google-maps/issues/287)) ([bea68f9](https://github.com/visgl/react-google-maps/commit/bea68f923e9326188baebd8a89b9ad5cbf891303)), closes [#285](https://github.com/visgl/react-google-maps/issues/285)

## [0.8.1](https://github.com/visgl/react-google-maps/compare/v0.8.0...v0.8.1) (2024-03-26)


### Bug Fixes

* InfoWindow.shouldFocus doesn't work with false as value ([#278](https://github.com/visgl/react-google-maps/issues/278)) ([2f4b508](https://github.com/visgl/react-google-maps/commit/2f4b508a3da87f778496043dc7d5b40f47837d1f))

## [0.8.0](https://github.com/visgl/react-google-maps/compare/v0.7.1...v0.8.0) (2024-03-20)


### Features

* add new prop InfoWindow.shouldFocus ([#254](https://github.com/visgl/react-google-maps/issues/254)) ([c83ea37](https://github.com/visgl/react-google-maps/commit/c83ea375295699ed4e3c3a4a6f097cad1a4aca7d))

## [0.7.1](https://github.com/visgl/react-google-maps/compare/v0.7.0...v0.7.1) (2024-02-23)


### Bug Fixes

* export api-loading-status types ([#231](https://github.com/visgl/react-google-maps/issues/231)) ([9695034](https://github.com/visgl/react-google-maps/commit/9695034d3c51936c2c701b7fb8be4a864f349c3e)), closes [#230](https://github.com/visgl/react-google-maps/issues/230)

## [0.7.0](https://github.com/visgl/react-google-maps/compare/v0.6.1...v0.7.0) (2024-02-15)


### ⚠ BREAKING CHANGES

* removed the `useStreetViewPanorama()` and `useDirectionsService()` hooks.

### Features

* add example for drawing tools ([#220](https://github.com/visgl/react-google-maps/issues/220)) ([75e91c4](https://github.com/visgl/react-google-maps/commit/75e91c4a3b3893ac3d97b5689682bcca5262aac9))
* restore map state when changing mapId ([#213](https://github.com/visgl/react-google-maps/issues/213)) ([0db363f](https://github.com/visgl/react-google-maps/commit/0db363f9c0291135b31ac387d4513bbaf652517a))


### Code Refactoring

* remove obsolete hooks ([#219](https://github.com/visgl/react-google-maps/issues/219)) ([69b2373](https://github.com/visgl/react-google-maps/commit/69b23734270e8754a518790620872dc1f4136cc7))

## [0.6.1](https://github.com/visgl/react-google-maps/compare/v0.6.0...v0.6.1) (2024-02-08)


### Bug Fixes

* remove deep-link into fast-deep-equal package ([#208](https://github.com/visgl/react-google-maps/issues/208)) ([f0be380](https://github.com/visgl/react-google-maps/commit/f0be3803eeb3aa0c80b19b42977e714dcb746a2f))

## [0.6.0](https://github.com/visgl/react-google-maps/compare/v0.5.4...v0.6.0) (2024-02-07)


### ⚠ BREAKING CHANGES

* The behaviour of the props controlling camera parameters (center, zoom, heading and tilt) changed. Unless you are using controlled props, you have to change the prop names from e.g. `center` to `defaultCenter` (the same goes for `zoom`, `heading` and `tilt`).

### Code Refactoring

* improved state-handling implementation ([#181](https://github.com/visgl/react-google-maps/issues/181)) ([904b918](https://github.com/visgl/react-google-maps/commit/904b918427da071477ed4bb8c2c65006b35dff88))

## [0.5.4](https://github.com/visgl/react-google-maps/compare/v0.5.3...v0.5.4) (2024-02-01)


### Bug Fixes

* prevent passing empty parameters to ApiLoader ([#193](https://github.com/visgl/react-google-maps/issues/193)) ([0601753](https://github.com/visgl/react-google-maps/commit/0601753c03539dc1180272b31aafab911ebe9c2c))

## [0.5.3](https://github.com/visgl/react-google-maps/compare/v0.5.2...v0.5.3) (2024-02-01)


### Bug Fixes

* add `loading=async` to maps API url ([cb1336f](https://github.com/visgl/react-google-maps/commit/cb1336fc97dda8b3ad99c3f9a9a560cf8186056b))
* use parameter `v` instead of `version` ([0626fb6](https://github.com/visgl/react-google-maps/commit/0626fb6411ada3293d0f4a640dff07d0e19fc805))

## [0.5.2](https://github.com/visgl/react-google-maps/compare/v0.5.1...v0.5.2) (2024-02-01)


### Bug Fixes

* trigger release for new library function from commit 31f2655 ([b5a13e5](https://github.com/visgl/react-google-maps/commit/b5a13e598d97ae65304df6f79d05247b847e670b))

## [0.5.1](https://github.com/visgl/react-google-maps/compare/v0.5.0...v0.5.1) (2024-01-31)


### Bug Fixes

* infowindow double rendering and eslint warnings ([#185](https://github.com/visgl/react-google-maps/issues/185)) ([404cc06](https://github.com/visgl/react-google-maps/commit/404cc06253a92f120f97f72179949a8f4c0fc87b))

## [0.5.0](https://github.com/visgl/react-google-maps/compare/v0.4.3...v0.5.0) (2024-01-18)


### Features

* handle API-key errors in map-component ([#165](https://github.com/visgl/react-google-maps/issues/165)) ([26ccc15](https://github.com/visgl/react-google-maps/commit/26ccc15d640346ce71157d387fbc56720234fa4c))


### Bug Fixes

* don't use potentially unreliable addListener functions ([#158](https://github.com/visgl/react-google-maps/issues/158)) ([7309efa](https://github.com/visgl/react-google-maps/commit/7309efa1db8b392ebe2840e5d527a92419c9fc2a))
* export event-types ([#167](https://github.com/visgl/react-google-maps/issues/167)) ([cdd6b72](https://github.com/visgl/react-google-maps/commit/cdd6b72f848bf5b54618862788e1a3a221fcdce1))
* export type properly ([#170](https://github.com/visgl/react-google-maps/issues/170)) ([e561031](https://github.com/visgl/react-google-maps/commit/e56103149f15977ae0e7f62dd359cd3759b71fc9))

## [0.4.3](https://github.com/visgl/react-google-maps/compare/v0.4.2...v0.4.3) (2024-01-05)


### Bug Fixes

* allow AdvancedMarker to accept space-separated multiple class names ([#143](https://github.com/visgl/react-google-maps/issues/143)) ([eab53e2](https://github.com/visgl/react-google-maps/commit/eab53e2ffa69325fb927b16d59f6aa7faa589a49))

## [0.4.2](https://github.com/visgl/react-google-maps/compare/v0.4.1...v0.4.2) (2023-12-22)


### Bug Fixes

* avoid re-render on every importLibrary() call ([#135](https://github.com/visgl/react-google-maps/issues/135)) ([32b5894](https://github.com/visgl/react-google-maps/commit/32b5894518a22793c236bcab33291f25b48f7367))

## [0.4.1](https://github.com/visgl/react-google-maps/compare/v0.4.0...v0.4.1) (2023-12-01)


### Bug Fixes

* move @types/google.maps to dependencies ([#115](https://github.com/visgl/react-google-maps/issues/115)) ([9b788e1](https://github.com/visgl/react-google-maps/commit/9b788e10722ecbc8d483313c7d746b90f67afc87)), closes [#106](https://github.com/visgl/react-google-maps/issues/106)
* output an error when useMap is called outside APIProvider ([#117](https://github.com/visgl/react-google-maps/issues/117)) ([5c30c3d](https://github.com/visgl/react-google-maps/commit/5c30c3d5a36af57a649ca3201f7dd0c3819e6035))

## [0.4.0](https://github.com/visgl/react-google-maps/compare/v0.3.3...v0.4.0) (2023-11-28)


### Features

* Allow &lt;Pin&gt; glyphs to be passed as children (close [#98](https://github.com/visgl/react-google-maps/issues/98)) ([#99](https://github.com/visgl/react-google-maps/issues/99)) ([6374453](https://github.com/visgl/react-google-maps/commit/637445313c8c9364cbf1f32346d3438fc0589d74))

## [0.3.3](https://github.com/visgl/react-google-maps/compare/v0.3.2...v0.3.3) (2023-11-13)


### Bug Fixes

* add map camera state tracking ([#84](https://github.com/visgl/react-google-maps/issues/84)) ([1dc1584](https://github.com/visgl/react-google-maps/commit/1dc158436c4ffde60548486da5410b46e989fc5b))

## [0.3.2](https://github.com/visgl/react-google-maps/compare/v0.3.1...v0.3.2) (2023-11-09)


### Bug Fixes

* use moveCamera and useLayoutEffect for faster map-updates ([e493d5f](https://github.com/visgl/react-google-maps/commit/e493d5ffa350efebddd5ef63bb57495954478877))

## [0.3.1](https://github.com/visgl/react-google-maps/compare/v0.3.0...v0.3.1) (2023-11-09)


### Bug Fixes

* update ControlPosition values ([#71](https://github.com/visgl/react-google-maps/issues/71)) ([1dd144a](https://github.com/visgl/react-google-maps/commit/1dd144ac3deac53a77d870ba8cf1e4623786a620))

## [0.3.0](https://github.com/visgl/react-google-maps/compare/v0.2.1...v0.3.0) (2023-11-09)


### ⚠ BREAKING CHANGES

* removed MapProps.onLoadMap

### Features

* cleanup map, remove onLoadMap prop ([d5e7dfd](https://github.com/visgl/react-google-maps/commit/d5e7dfdf74d76395ffbc1bcd2afda62a12eb7e57))
* implement props for all map-events with custom MapEvent type ([820a301](https://github.com/visgl/react-google-maps/commit/820a301e4a30e2b7bbbe7c82c69675f9c410813e))
* update map viewport when props are changed ([0b1d800](https://github.com/visgl/react-google-maps/commit/0b1d800dc5e4b9bf0b1ddb42b9fed392b23b8dae))

## [0.2.1](https://github.com/visgl/react-google-maps/compare/v0.2.0...v0.2.1) (2023-11-07)


### Bug Fixes

* add types to package exports ([#62](https://github.com/visgl/react-google-maps/issues/62)) ([1ab493a](https://github.com/visgl/react-google-maps/commit/1ab493a71ddaeff3b31caec10be1fd4728d51362))

## [0.2.0](https://github.com/visgl/react-google-maps/compare/v0.1.2...v0.2.0) (2023-11-07)


### Features

* new MapControl component ([#51](https://github.com/visgl/react-google-maps/issues/51)) ([7eb49ed](https://github.com/visgl/react-google-maps/commit/7eb49ed55eb548c342f83bcdbf9dc655655bafe7))
* standalone examples (CodeSandbox) ([#48](https://github.com/visgl/react-google-maps/issues/48)) ([959c6e3](https://github.com/visgl/react-google-maps/commit/959c6e3d57d896d4f76640e01b3ad0a33dea3fae))


### Bug Fixes

* replace prop `gmpDraggable` with `draggable` in AdvancedMarker ([#53](https://github.com/visgl/react-google-maps/issues/53)) ([1dbf477](https://github.com/visgl/react-google-maps/commit/1dbf477dfa2e471edf9a9daacd5e5e384a48d8de))
* update usage of useMapsLibrary in AdvancedMarker ([#55](https://github.com/visgl/react-google-maps/issues/55)) ([b01fc8b](https://github.com/visgl/react-google-maps/commit/b01fc8bbafae569fbb21a3175deb5b66762eb083))

## [0.1.2](https://github.com/visgl/react-google-maps/compare/v0.1.1...v0.1.2) (2023-11-01)


### Miscellaneous Chores

* add registry-url to release action ([9fa403b](https://github.com/visgl/react-google-maps/commit/9fa403bd4d6dfc31b84683543868b0bfbe70e2b9))

## [0.1.1](https://github.com/visgl/react-google-maps/compare/v0.1.0...v0.1.1) (2023-11-01)


### Bug Fixes

* empty commit to trigger release-please ([b04a942](https://github.com/visgl/react-google-maps/commit/b04a9421fc290c3ca6eacc02391726beab4bba4b))

## [0.1.0](https://github.com/visgl/react-google-maps/compare/v0.0.5...v0.1.0) (2023-10-27)


### ⚠ BREAKING CHANGES

* loading multiple libraries at once is no longer supported, changed the return type of useMapsLibrary.

### Features

* useMapsLibrary returns API object instead of boolean ([#26](https://github.com/visgl/react-google-maps/issues/26)) ([a3aa4c5](https://github.com/visgl/react-google-maps/commit/a3aa4c5e10228003206c8de3305f857df50d73d1))
