---
layout: post
title:  "Book notes: The Pragmatic Programmer"
categories: book-notes
author: "Nathan Kane"
date:   2016-03-07
comments: true
---

Yo yo yo
--------

Here is some code:
{% highlight javascript linenos %}

import actions from '../actions';

const ProductItemContainer = React.createClass({
  onAddToCartClicked() {
    actions.addToCart(this.props.product);
  },

  render() {
    return (
      <ProductItem product={this.props.product} onAddToCartClicked={this.onAddToCartClicked} />
    );
  }
});

// comments are good

export default React.createClass({
  mixins: [reactor.ReactMixin],

  getDataBindings() {
    return {
      products: getters.products,
    }
  },

  render: function () {
    return (
      <ProductsList title="Flux Shop Demo (NuclearJS)">
        {this.state.products.map(product => {
          return <ProductItemContainer key={product.get('id')} product={product.toJS()} />;
        }).toList()}
      </ProductsList>
    );
  },
});

{% endhighlight %}
