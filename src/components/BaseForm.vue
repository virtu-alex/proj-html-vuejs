<template>
  <div class="col-7">
    <h5>Send a message</h5>
    <h1 class="py-3">Get in Touch</h1>
    <p class="py-3">We will respond to your message as soon as possible.</p>

    <form role="form">
      <div class="controls">
        <div class="row">
          <div class="col-md-6">
            <div class="form-group">
              <input
                type="text"
                name="name"
                class="form-control form-color"
                placeholder="Name"
              />
            </div>
          </div>
          <div class="col-md-6">
            <div class="form-group">
              <input
                type="text"
                name="email"
                class="form-control"
                placeholder="Email"
              />
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-6 py-3">
            <div class="form-group">
              <input
                type="phone"
                name="phone"
                class="form-control"
                placeholder="Phone"
              />
            </div>
          </div>
          <div class="col-md-6 py-3">
            <div class="form-group">
              <select id="form_need" name="need" class="form-control">
                <option selected disabled value="">More Info</option>
                <option>Request Invoice for order</option>
                <option>Request order status</option>
                <option>Haven't received cashback yet</option>
                <option>Other</option>
              </select>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-12">
            <div class="form-group">
              <textarea
                class="form-control"
                placeholder="Write your message here."
                rows="4"
              ></textarea>
            </div>
          </div>
          <div class="col-md-12 py-3">
            <input
              type="submit"
              class="btn btn-success btn-send pt-2 btn-block"
              value="Send"
            />
          </div>
        </div>
      </div>
    </form>
  </div>
</template>
<script>
  export default {
    name: "BaseForm"
  };
</script>
<style lang=""></style>
